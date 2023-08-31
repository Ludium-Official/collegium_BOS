# Collegium-BOS-WK1

## 주제: 컴포넌트와 컴포지션 만들어보기
이번 과제는 이름을 입력하고 친근한 인사말을 렌더링하는 간단한 애플리케이션을 만듭니다.

## 1. 온라인 에디터 환경 접속하기
1. [jutsu](https://jutsu.ai/) 사이트에 접속해주세요.

2. TRY FOR FREE 버튼을 클릭해주세요.

![TRY FOR FREE](assets/images/nearpad.png)

3. [jutsu 편집기](https://jutsu.ai/editor)가 나타나는 것을 확인해주세요.

![nearpad_editor](assets/images/nearpad_editor.png)

## 2. 새 컴포넌트 만들기
1. Crerate Widget 버튼을 클릭해주세요.

![create_widget](assets/images/create_widget.png)

## 3. 지갑 연결하기
1. Connect 버튼을 클릭해주세요.

![connect_button](assets/images/connect_button.png)

2. 사용할 지갑을 선택해주세요. (ex: NEAR Wallet을 선택)

![select_wallet](assets/images/select_wallet.png)

3.Next 버튼을 클릭해주세요

![connect_dialog](assets/images/connect_dialog.png)

4. Connect 버튼을 클릭해주세요.

![connect_near_dialog](assets/images/connect_near_dialog.png)

## 4. Greeter 위젯을 불러오기
1. search component button을 클릭해주세요.

![search_component_button](assets/images/search_component_button.png)

2. `idknwhoru.near/widget/greeter` 을 검색 해주세요 

![search_component](assets/images/search_component.png)

3. fork widget 버튼을 클릭해주세요.

![fork_widget_button](assets/images/fork_widget_button.png)

4. Open Widget 목록에 Greeter 위젯이 추가된 것을 확인해주세요.

![add_greeter_widget](assets/images/add_greeter_widget.png)

5. Greeter 위젯에 작성된 코드를 확인해주세요.

![greeter_code](assets/images/greeter_code.png)

## 5. Greeter 위젯에 Props를 전달하기
1. Props 탭을 선택해주세요.

![props_tab](assets/images/props_tab.png)

2. props 에디터에 아래 내용을 추가해주세요.
``` json
{
  "name": "WHORU"
}
```
3. Preview 탭에 표시되는 화면이 바뀐것을 확인해주세요.

![preview_whoru](assets/images/preview_whoru.png)

## 6. Composition 컴포넌트 만들기
1. Add new button 버튼을 클릭해주세요.

![add_new_button](assets/images/add_new_button.png)

2. 컴포넌트 이름을 Composition으로 변경해주세요.
3. rename 버튼을 클릭해주세요.

![composition_component](assets/images/composition.png)

4. 아래 코드를 Composition의 코드에 추가해주세요.
``` jsx
// user의 값은 자신의 지갑 주소를 입력해주세요.
const user = "idknwhoru.near";

return (
  <>
    <h3> Composition </h3>
    <p> Components can be composed </p>
    <hr />
    {/** 자신이 만든 Greeter 컴포넌트를 불러올 수 있습니다. **/}
    <Widget src={`${user}/widget/Greeter`} props={props} />
  </>
);
```

5. Previe에 `Greeter` 위젯이 포함된 컴포지션이 화면에 나타나는지 확인해주세요.

![preview_composition](assets/images/preview_composition.png) 

6. Publish 버튼을 클릭해주세요.

![publish_button](assets/images/publish_button.png)

7. Saving data 대화 상자가 나타나는 것을 확인해주세요.

![Alt text](assets/images/saving_data_composition_dialog.png)

8. Save data 버튼을 클릭해주세요.

![save_data_button](assets/images/save_data_button.png)

9. My Widget에 Composition이 추가된 것을 확인해주세요.

![my_widget_composition](assets/images/my_widget_composition.png)

## Mission
- [ ] Greeter 위젯의 이름을 `GreetingYourName`으로 바꿔보세요.

![greeting_your_name](assets/images/greeting_your_name.png)

- [ ] `idknwhoru.near/widget/GreeterToday`을 fork 하고 실행 화면을 `Hello Agwn! Today is 07-09-2023` 바꿔보세요.

![preview_greeting](assets/images/preview_greeting.png)

- [ ] Composition에 포함된 위젯을 `idknwhoru.naer/widget/Greeter`에서 다른 위젯으로 바꿔보세요.(위젯을 검색하는 방법은 4. Greeter 위젯 불러오기와 6. Composition 만들기를 참고)

![container_load_harmonicHomPage](assets/images/container_load_harmonicHomPage.png)
