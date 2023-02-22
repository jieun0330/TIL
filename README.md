# TIL
Today what I Learned...


var와 let의 차이점에 대해 서술하고 그 예제 코드 작성

var(변수, 변할 수 있는 값)
 : 선언 시 처음 입력된 데이터 이후 추가로 입력 간으하며, 마지막에 입력된 데이터가 최종 데이터가 됩니다.
 : 이후에 수정, 새로운 값을 할당이 가능한 것
 : 값을 수정할 수 있다.

let(상수, 변하지 않는 값, 고정된 값)
 : 선언 시 처음 입력된 데이터만 저장하게 됩니다.
 : 수정이 불가한 것
 
 상수를 사용하는 이유는 다양하지만, 그 중 가장 중요한 이유는 가독성이다.
 : 상수로 값을 선언하면, 이후 코드에서 이 값은 변화가 없다는 사실을 굳이 주석이나 api 문서를 확인하지 않고도 바로 알 수 있다.

//var number2 : Int = 20
//number2 = 30
//print(number2)

//let number1 : Int = 10
//number1 = 0
//print(number1)
//number1에 입력된 데이터는 변하지 않음

/*
 그러면 스위프트나 다른 언어들에서 왜 이렇게 불변하는 변수를 만들까?
 그냥 전부 다 var로 하면 편할텐데 말이다.
 이는 바로 효율성, 성능 때문이다.
 
 변하면 안되는 값을 변경하는 실수를 막아줄 수 있습니다.
 
 내가 마트에 가서 매일 식빵을 2개 사온다고 생각해보자.
 var라는 장바구니는 얼마나 많은 식빵이 들어올지 모르고
 여러 경우를 대비해야하기 때문에 무지막지하게 큰 장바구니를 들고 다니는 것이다.
 그러나 let은 딱 식빵 2개 들어갈 수 있는 장바구니를 만드는 것이다.
 
 핸드폰 용량을 표시해주는 app을 개발하게 될 때, 전체 공간의 용량을 let 상수로 저장하고, 사용 가능 공간을 var 변수로 저장할 것이다.이렇게 변하지말아야할 값을 상수로 선언하므로써 컴파일러가 자동으로 오류를 발생시키게 함으로써 스위프트 언어의 안전성을 보장받을 수 있다.
*/










//반복문(Loop)의 종류와 1~10까지 출력하는 코드 작성

//for문
//for x in 1...100{
//    print(x)
//}




//var total : Int = 0
//for x in 1...100{
//    print(x)
//    total = total + x
//}
//print("total = \(total)")





//let forRange = 0...10
//
//var sum = 0
//for i in forRange{
//    print(" \(i)")
//    sum += i
//}
//print("sum: \(sum)")






//var sum = 0
//for i in 0...10{
//    if i <= 0 {
//        continue
//    }
//    
//    print("\(i)")
//    sum += i
//}
//print("sum: \(sum)")





//var sum = 0
//for i in 0...10 {
//    if i == 3{
//        break
//    }
//
//    print("\(i)")
//    sum += 1
//}
//
//print("sum: \(sum)")






//let counts = 1...10
//
//for _ in counts{
//    print("Repeat")
//}







//
//outermostLoop : for i in 1...10 {
//    for j in 1...10 {
//        for k in 1...10 {
//            let volume = i * j * k
//            print("\(i) * \(j) * \(k) is volume")
//
//            if volume == 50 {
//                print("Stop repeat! I want this volume.")
//                break outermostLoop
//            }
//        }
//    }
//}







//let saladIngredients: Array<String> = ["tomato", "onion", "sweet potato", "celery", "cucumber", "chicory", "olive", "beet"]
//var mySalad : Array<String> = Array<String>()
//
//for vegetable in saladIngredients {
//    if vegetable == "cucumber"{
//        print("\(vegetable)? oh, take it out.")
//        continue
//    }
//    mySalad.append(vegetable)
//}
//
//print(mySalad)







//var age = 19
//var student = ""
//
//if age >= 8 && age < 14 {
//    student = "초등학생"
//} else if age < 17 {
//    student = "중학생"
//} else if age < 20 {
//    student = "고등학생"
//} else {
//    student = "기타"
//}
//
//
//print(student)






//for _ in 0..<10 {
//    print("Hello")
//}








//let alphabet : [String] = ["a", "b", "c", "d"]
//
//for char in alphabet {
//    print(char)
//}








//for i in 0...4 {
//    print(i)
//}






//let people = ["Tom" : 22, "Harry" : 24, "Jane" : 20]
//
//for (name, age) in people {
//    print("\(name) is \(age) years old!")
//}






//for i in 0...4 {
//    if i <= 0 { continue };
//    print(i)
//}
//i가 0 이하인 경우에는 다음 print 로직을 실행하지 않고, 이 외의 경우 1, 2, 3만 실행된 모습이다.







//for i in 0...5 {
//    if i == 3 { break };
//    print(i)
//}







//var arrayUser = ["유저1", "유저2", "유저3"]
//var dictionaryUser = ["1번" : "유저1", "2번" : "유저2", "3번" : "유저3"]
//
//for users in arrayUser {
//    print(users)
//}
//
//
//for (key,name) in dictionaryUser {
//    print("\(key) : \(name)")
//}










//for index in 0..<10 {
//    print("\(index)번째")
//}










//let closedRange = 0...10
//for i in closedRange where i % 2 == 0 {
//    print("i의 짝수 : \(i)")
//}










//let closedRange = 0...10
//for i in closedRange {
//    if i == 4 {
//        continue
//    }
//    if i == 6 {
//        break
//    }
//    print("4 제외 : \(i)")
//}
//continue는 해당 조건을 건너뛰라는 뜻이며, break는 종료를 뜻합니다.









/*
 while문
 : 조건식을 검사하여 조건식이 참이면 계속 검사를 진행하고, 거짓일 경우 while문을 종료합니다.
 */
//var start = 1
//while start <= 10{
//    print(start)
//    start += 1
//}






//var k = 0
//for i in 0...10 {
//    if i % 2 == 0 {
//        print("짝수: \(i)")
//    }
//    k += 1
//}
//print("반복횟수: \(k)")
//
//
//k = 0;
//for i in 0...10 where i % 2 == 0 {
//    print("짝수: \(i)")
//    k += 1
//}
//print("반복 횟수 : \(k)")






//var count = 1
//
//while count <= 10{
//    print(count)
//    count += 1
//}
//for문과는 다르게 반복 조건의 값은 boolean 타입으로 평가되어야 합니다.







//let range = 0...100
//var currentPosition = 0
//
//while currentPosition <= 100 {
//    print(currentPosition)
//    if currentPosition == 10{
//        print("Enough, stop!")
//        break
//    }
//    currentPosition += 1
//}










//let name : [String] = ["song", "kim", "park", "chang"]
//
//var i : Int = 0
//while i < 4 {
//    print("name is \(name[i])")
//    i += 1
//}








//var j = 10
//
//while j < 10 {
//    print(j)
//}
//
//repeat {
//    print(j)
//    j += 1
//} while j < 10





//while true {
//    print("무한 실행...")
//}

//var count = 0
//
//while count < 3 {
//    count += 1
//
//    print("3보다 값이 작을 때까지 반복문이 실행된다.")
//}









//var count = 0
//
//repeat {
//    print("일하자,,")
//    count += 1
//} while count < 5
//    print("퇴근 :)")










//var i = 0
//while i < 10 {
//    i += 1
//    print("\(i)번째 출력!")
//}










//var i = 0
//while true {
//    i += 1
//    if i > 100 {
//        break
//    }
//    print("\(i)번째 출력")
//}














/*
 for문과 while문의 차이
 : for문은 일정 횟수 동안 반복해야 하는 경우
 : while문은 일정 조건이 유지되는 동안
 
 for문은 반복을 멈춰야 하는 시점을 아는 경우,
 while문은 반복을 멈춰야 하는 시점이 정해져 있지 않은 경우
 */






//조건을 검사할 때에는 if, switch를 씁니다.

//var age = 13
//var student = ""
//
//switch age {
//case 8..<14:
//    student = "초등학생"
//case 14..<17:
//    student = "중학생"
//case 17..<20:
//    student = "고등학생"
//default:
//    student = "기타"
//}
//
//print(student)












//let range = [1,2,3,4,5,6]
//
//for i in range where i % 2 == 0 {
//    print(i)
//}









//var count = 0
//
//while count < 5 {
//    count += 1
//
//    if(count == 3) {
//        print("count 값이 3이라면 while 탈출")
//        break
//    }
//    print ("탈출 실패 count 값 : \(count)")
//
//    if(count != 3){
//        print("count 값이 3이 아니다")
//        continue
//    }
//
//}
//print("탈출 성공")











//타입 추론(Type Inference)이란?

/*
 타입추론은 타입을 직접 명시하지 않아도 컴파일러가 초기화된 값을 보고 타입을 추론하는 것을 말합니다.
 타입추론을 하게되면 타입을 지정해주는 것보다 시간이 좀 더 걸린다고 합니다.
 또한, 타입을 지정하지 않았을 때, 발생하는 오류로 인해 시간을 많이 잡아먹을 수 있기 때문에 처음부터 타입을 지정해주는 것이 좋다고 합니다.
 */










//논리연산자(Boolean Logic)인 AND(&&)와 OR(||)로 나올 수 있는 경우의 수 4가지


let enteredDoorCode = true
let passedRetinaScan = false

if enteredDoorCode && passedRetinaScan {
    print("Welcome")
} else {
    print("ACCESS DENIED")
}






let hasDoorKey = false
let knowsOverridePassword = true

if hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}





if enteredDoorCode && passedRetinaScan || hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}





if (enteredDoorCode && passedRetinaScan) || hasDoorKey || knowsOverridePassword {
    print("Welcome!")
} else {
    print("ACCESS DENIED")
}
