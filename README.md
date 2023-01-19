// Todo-list

let input = prompt("무엇을 입력하시겠습니까?");
const todos = ['몽이 산책시키기', '요리하기', '코딩 공부'];

while(input !== 'quit' && input !== 'q'){
    if(input === 'list') {
        console.log("********************");
        for(let i = 0; i < todos.length; i++){
            console.log(`${i}: ${todos[i]}`);
        }
        console.log("********************");
    } else if (input === 'new'){
        const newTodo = prompt("새로 하고 싶은 일은 무엇입니까?");
        todos.push(newTodo);
        console.log(`${newTodo} 가 리스트에 추가되었습니다.`)
    } else if(input === 'delete'){
        const index = parseInt(prompt("지우고자 하는 인덱스 번호를 입력해주세요:"));
        if(Number.isNaN(index)){
            console.log("알 수 없는 인덱스 입니다.");
        } else {
            const deleted = todos.splice(index, 1);
            console.log(`입력하신 할 일이 삭제되었습니다. ${deleted[0]}`);
        } 
        
    } 
    input = prompt("무엇을 입력하시겠습니까?");
}
console.log("어플을 종료합니다.")
