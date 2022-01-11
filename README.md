nomadcoder의 ReactJS로 영화 웹 서비스 만들기를 보고 정리
<br>
<https://nomadcoders.co/react-for-beginners/lobby>
<br>
<br>

# react-basis
1. ReactJS는 JS와 반대이다. ReactJS는 JS를 HTML로 바꾸는 반면, JS는 JS에 HTML을 가져와 사용한다.
2. reactJS는 바뀐 부분만 다시 랜더링하지만 JS는 body 전체를 다시 랜더링한다.
3. react-dom: JS에 작성한 것을 HTML로 바꾸어준다.
4. 직접 만든 컴포넌트의 이름은 대문자로 시작해야 한다. 그래야 컴포넌트로 인식할 수 있다. 대문자를 사용하지 않으면 HTML태그로 인식하기도 한다.
5.  속성이 다른 것이 있다. ex) class -> className, for -> htmlFor
<br>
<br>

# state
### [ state 값 설정하는 2가지 방법 ]
1. `setCounter(counter+1);`
2. `setCounter((current) => current +1);`
<br>
2가 더 안전하다 항상 현재값을 보장하기 때문이다.

### [ form에서 react 다루기 ]
1. input태그 안에 value={}와 이벤트 리스너 추가
2. vlaue안에 넣을 변수를 setState로 만든다.
3. 이벤트 리스너 안에 event인자를 이용해 event.target.value로 value에 접근해 setState()의 함수로 value값을 바꿀 수 있다.

<br>
- setState()로 만든 변수는 여러군데서 사용할 수 있고 minutes/60과 같은 연산을 해도 자동으로 계산해준다.
<br>
- reset 버튼을 만들 때, setState()의 함수를 0값으로 지정해 활용하는 방법이 있다.
<br>
<br>

# props
> 부모 컴포넌트로부터 자식 컴포넌트에 데이터를 보낼 수 있게 해주는 방법
- props는 첫 번째 인자이자 유일한 인자다.
- props는 내가 부모 컴포넌트에서 보낸 모든 것들을 갖는 오브젝트이다.
<br>
<br>
### [ props로 값을 전달하는 2가지 방법]
1. (props)로 전달해 props.으로 접근해 사용한다.
2. ({...}) 안에 직접 인자들을 전달한다. props.을 사용하지 않아도 되어 편하다.

### [propsTypes]
> props의 타입을 지정, 틀리면 warning을 띄어준다.
- 다양한 타입들이 존재
- 꼭 필요한 것을 입력받을 수 있게 할 수 있다.
<br>
<br>

# 이외
## [ React.memo ]
부모의 props에 변화가 일어나면 모든 자식들이 다시 랜더링이 된다. 하지만, memo를 사용하면  자식들도 바뀌는 것만 다시 랜더링이 되어 속도가 느려지는 것을 막을 수 있다.
