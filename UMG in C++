// this is for creating umg in c++ basics.

void UMyEditorWidgetClass::NativePreConstruct() { 
  Super::NativePreConstruct();
  // The default root widget is a canvas panel
  UWidget* RootWidget = GetRootWidget();
  UCanvasPanel* CanvasPanel = static_cast(RootWidget);
  // Here we create a text block
  UTextBlock* TextBlock = NewObject(); 
  TextBlock->SetText(FText::FromString("Hello World"));
  // Then a button which contains the text block
  UButton* Button = NewObject();
  Button->SetContent(TextBlock);
  Button->OnClicked.AddDynamic(this, &UMyEditorWidgetClass::PrintText);   
  CanvasPanel->AddChildToCanvas(Button);
}
