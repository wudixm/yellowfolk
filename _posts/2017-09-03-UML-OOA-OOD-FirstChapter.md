---
title: 第一章 基于面向对象对象的UML
excerpt: |
  第一章 基于面向对象对象的UML
category: 分析与设计
feature_image: "https://picsum.photos/2560/600?image=872"
---
UML是一种在多种面向对象建模方法的基础上发展的**通用可视化建模语言**，它拥有一整套完成而成熟的建模技术，被广泛地运用于各种不同领域，**借助于基于面向对象的UML，可以帮助软件工程的开发人员更好地理解业务流程，建立更可靠、更完善的系统模型，**从而方便我们对各种软件工程进行正确的描述和交流。

## 面向对象是UML的基础

**UML统一建模语言的出现正是由于面向对象建模思想发展的产物，它是软件工程领域公认的面向对象的建模语言。**可以毫不夸张地说，没有面向对象，就没有UML。它们的关系是如此的密不可分。

### 什么是面向对象

**面向对象程序设计（Object-Oriented Programming，OOP）立足于创建软件代码的重复使用，具备更好地模拟现实世界环境的能力，**这使它被公认为是自上而下编程的最佳选择。

1. 什么是对象

   对象（Object）是面向对象（Object-Oriented，OO）系统的基本构造块，是一些相关的变量和方法的软件集。对象经常用于建立现实世界中我们身边的一些对象的模型。对象是理解面向对象的技术的关键。

   **在软件工程设计中的对象，是指一种将状态和行为有机结合起来形成的软件构造模型，它可以用来描述或代表现实世界中的一个对象。软件对象其实就是现实世界对象的一种模型，它有自己的状态和行为。**

2. 面向对象与面向过程的区别

   在面向对象程序设计（OOP）方法之前，结构化程序设计占据主要的地位。**结构化程序设计思想就是把大的程序分解成具有层次结构的若干个模块，每个模块再分解为下一层模块，如此自顶向下，逐步细分，把复杂的大模块分解为许多功能单一的小模块。结构化程序设计特征就是以函数为中心，也就是以功能为中心来描述系统，用函数来作为划分程序的基本单位，数据在过程式设计中往往处于从属的位置。**

   结构化程序设计的优点是易于理解和掌握，这种模块化、结构化、自顶向下、逐步求精的设计原则与大多数人的思维和解决问题的方式比较接近。

   但是，**对于比较复杂的问题，或在开发中需求变化比较多的时候，结构化程序设计往往显得力不从心。**事实上，**开发一个系统的过程往往也是一个对系统不断了解和学习的过程，而结构化程序设计是自上而下的，这要求设计者在一开始就要对需要解决的问题有一定的了解。在问题比较复杂的时候，要做到这一点会比较困难。**当开发中需求发生变化的时候以前对问题的理解也许会变得不再适用。

   **结构化程序设计的方法把密切相关、相互依赖的数据和对数据的操作相互分离，这种实质上的依赖与形式上的分离也使得大型程序的编写比较困难，难于调试和修改。**在由很多人进行协同开发的项目组中，程序员之间很难读懂对方的代码，代码的重用变得十分困难。由于现代应用程序的规模越来越大，对代码的可重用性和易维护性要求也越来越高，面向对象技术对这些提供了很好的支持。

   **面向对象技术是一种以对象为基础，以事件或消息来驱动对象执行处理的程序设计技术。**从程序设计方法上来讲，**它是一种自下而上的程序设计方法，它不像面向过程程序设计那样一开始就需要使用一个主函数来概括出整个程序，面向对象程序设计往往从问题的一部分着手，一点一点地构建出整个程序。**

   **面向对象设计是以数据为中心，使用类作为表现数据的工具，类是划分程序的基本单位。而函数在面向对象设计中成了类的接口。**

   **以数据为中心而不是以功能为中心来描述系统，相对来说，更能使程序具有稳定性。它将数据和对数据的操作封装到一起，作为一个整体进行处理，并且采用数据抽象和信息隐藏技术，最终被抽象成一种新的数据类型——类。**

   类与类之间的联系以及类的重用出现了类的继承、多态等特性。类的集成度越高，越适合大型应用程序的开发。

   **面向对象程序的控制流程运行时是由事件进行驱动的，而不再由预定的顺序进行执行。事件驱动程序的执行围绕消息的产生与处理，靠消息的循环机制来实现。更重要的是，可以利用不断成熟的各种框架，如.NET的.NET Framework等，迅速地将程序构建起来。面向对象的程序设计方法还能够使程序的结构清晰简单，能够大大提高代码的重用性，有效地减少程序的维护量，提高软件的开发效率。**

   在结构上，面向对象程序和结构化程序设计也有很大的不同。**结构化程序设计首先应该确定的是程序的流程怎样走，函数间的调用关系怎样，以及函数间的依赖关系是什么。**一个主函数依赖于其子函数，这些子函数又依赖于更小的子函数，而在程序中，越小的函数处理的往往是细节实现，**这些具体的实现又常常变化。这样的结果，就是程序的核心逻辑依赖于外延的细节，程序中本来应该是比较稳定的核心逻辑，也因为依赖于易变化的部分，而变得不稳定起来，**一个细节上的小小改动，也有可能在依赖关系上引发一系列变动。**可以说这种依赖关系也是过程式设计不能很好处理变化的原因之一，而一个合理的依赖关系应该是倒过来，由细节实现依赖于核心逻辑才对。**而面向对象程序设计由类的定义和类的使用两部分组成，**主程序中定义对象并规定它们之间的消息传递方式，程序中的一切操作都通过面向对象的发送消息机制来实现。对象接收到消息后，启动消息处理函数完成相应的操作。**

   以“仓库管理系统”为例，使用结构化程序设计方法的时候，首先要在主函数中确定仓库管理要做哪些事情，分别使用函数将这些事情进行表示，使用一个分支选择程序进行选择，然后再将这些函数进行细化实现，确定调用的流程等。

   **而在使用面向对象技术来实现的仓库管理系统中，以领取仓库物品的员工为例。首先要了解该员工的主要属性，如工号、所属部门等；其次要确定该员工要做什么操作，如领取或外借物料、办理手续等。并且把这些当成一个整体进行对待，形成一个类，即员工类，使用这个类，可以创建不同的员工实例，也就是创建许多具体的员工模型，每个员工拥有不同的工号，一些员工在不同的部门，都可以在仓库中领取材料或物品。员工类中的数据和操作都是给应用程序进行共享的，可以在员工类的基础上派生出普通员工类、部门经理类、总经理等，这样可以实现代码的重用。**

3. 对象与类的确定

   **面向对象技术认为客观世界是由各种各样的对象组成的，每个对象都有自己的数据和操作，不同对象之间的相互联系和作用构成了各种系统。**在面向对象的程序设计中，**系统被描绘成一系列完全自治、封装的对象组成，对象和对象之间是通过对象暴露在外的接口进行调用的。对象是组成系统的基本单元，是一个组织形式的含有信息的实体。而类是创建对象的模板，在整体上可以代表一组对象。**

   **设计类而不是设计对象就可以避免重复编码，类只需要编码一次，就可以被实例化属于这个类的无数个对象。**

   **对象是由状态（Attribute）和行为（Behavior）构成的。实际上，状态、属性（Property）、数据（Data）等这些在各种书中提到的概念，都是用于描述一个对象的数据元素，这些概念具体到各种语言便有不同的叫法。对象的状态值用来定义对象的状态。**

   行为、操作（Operation）以及方法（Method）这些在各种书中提到的概念，是用于描述用以访问对象的数据或修改/维护数据值的方法。

   **对象只有在具有状态和行为的情况下才有意义，“状态”用来描述对象的静态特征，“行为”用来描述对象的动态特征。对象是包含客观事物特征的抽象实体，封装了状态和行为。在程序设计领域，可以用“对象 = 数据 + 数据的操作”来进行表达。**

   **类（Class）是具有相同属性和操作的一组对象的组合。也就是说，抽象模型中的“类”描述了一组相似对象的共同特征，为属于该类的全部对象提供了统一的抽象描述。**

   类的定义要包含以下要素：

   - 定义该类对象的数据结构（属性的名称和类型）。
   - 对象所要执行的操作，也就是类的对象要被调用执行哪些操作，以及执行这些操作时对象要执行哪些操作，如数据库操作等。

   类是对象集合的抽象，类与对象的关系如同一个模具和使用这个模具浇注出来的铸件一样，**类是创建软件对象的模板——一种模型。类给出了属于该类的全部对象的抽象定义。而对象是符合这种定义的一个实体。类用来在内存中开辟一个数据区，存储新对象的属性；把一系列行为和对象关联起来。**

   **一个对象又被称做类的一个实例，也称为实体化（Instantiation）。术语“实体化（Instantiation）”是指对象在类声明的基础上创建的过程。**例如，声明了一个“员工”类，可以在这个基础上创建“一个姓名叫李平的员工”这个对象。

   **类的确定和划分没有一个统一的标准和方法，基本上依赖于设计人员的经验、技巧以及对实际项目中问题的把握。通常的标准是“寻求共性、抓住特性”，即在一个大的系统环境中，寻求事物的共性，将具有共性的事物用一个类进行表述。在具体的程序实现时，具体到某一个对象，要抓住对象的特性。**

   确定一个类通常包含以下方面：

   - 确定系统的范围，如仓库管理系统，需要确定一下和仓库管理相关的内容。
   - 在系统范围内寻找对象，该对象通常具有一个或多个类似的事物。例如，仓库管理系统中，有一个某部门名叫李平的员工，某部门名叫章飞的人是和李平类似的，都是普通员工。
   - 将对象抽象成为一个类，按照上面的类的定义，确定类的数据和操作。

   在面向对象程序设计中，类和对象的确定是软件开发非常重要的一步，类和对象的确定直接影响软件设计的优劣。如果划分得当，对象软件的维护与扩充以及软件的重用性都非常重要。

4. 消息和事件

   当使用某一个系统的时候，单击一个按钮，通常会显示相应的信息。在这个过程中，**首先要触发一个事件，然后，发送消息，那么什么是消息呢？所谓消息（Message），是指描述事件发生的信息，是对象间相互联系和相互作用的方式。一个消息主要由5部分组成：消息的发送对象、消息的接收对象、消息传递方式、消息内容（参数）、消息的返回。传入消息内容的目的有两个：一个是让接受请求的对象获取执行任务的相关信息，另一个是行为指令。

   **所谓事件，通常是指一种由系统预告定义而由用户或系统发出的动作。事件作用于对象，对象识别事件并作出相应反应。与对象的方法集可以无限扩展不同，事件的集合通常是固定的，用户不能随便定义新的事件。**但在现代高级语言中通过一些其他的技术可以在类中进行事件的加入。最熟悉的事件就是，用鼠标左键单击对象时发生的事件Click和界面被加载到内存中时发生的Load事件等。

   **对象通过对外提供的方法在系统中发挥自己的作用，当系统中的其他对象请求这个对象执行某个方法时，就向该对象发送一个消息，对象响应这个请求，完成指定的操作。程序的执行取决于事件的发生顺序，由顺序产生的消息来驱动程序的执行，不必预先确定消息产生的顺序。**

### 面向对象的基本特征

**面向对象技术强调的是在软件开发过程中，对于客观世界或问题域中的事物的认知，采用人类在认知客观世界的过程中普遍运用的思维方法，直观、自然地描述有关事物。**

**抽象、封装、继承、多态是面向对象程序的基本特征。正是这些特征使得程序的安全性、可靠性、可重用性和易维护性得以保证。**随着技术的发展，把这些思想用于硬件、数据库、人工智能技术、分布式计算、网络、操作系统等领域，越来越显示出其优越性。

1. 抽象

   我们的大脑懂得如何去简化所接收的信息，从中提取出重要的部分，让信息细节通过抽象（Abstraction）过程进行管理。通过抽象可以做到以下几点：

   1. **将需要的事物进行简化。通过抽象能够识别和关注当前状况或物体的主要特征。淘汰掉所有非本质信息。**也就是说，通过抽象可以忽略事物中与当前目标无关的非本质特征，强调与当前目标有关的特征。同时抽象与真实世界的不同，特征是根据使用对象的不同或者说是使用者类型不同进行确定的。

      以仓库管理系统为例，**从员工的角度来看，关注的是仓库管理系统能否领取或借到需要的物料。对于仓库管理人员，关注的往往是能否更好地管理好仓库和物品等。**

   2. **将事物特征进行概括。如果能够从一个抽象模型中剔出足够多的细节，那么它将变得非常通用，能够适用于多种情况或场合。这样的通用抽象常常相当有用。**例如，以员工为例，抽象出“工号”、“姓名”、“所属部门”、“职位”等来描绘员工，能够描绘出员工的一般功能，但是要具体到员工在企业里的工作地点等，描述力就差了一点。

      **抽象模型越简单，展示的特点越小，它就越通用，也越具有普适性。**抽象越复杂，越具有限制性，用于描述的情况也就越少。

   3. **将抽象模型组织为层次结构。能够通过抽象按照一定的标准将信息系统地进行分类处理，依此来应付系统的复杂性。**这一过程被称为分类（Classification）。

      例如在科学领域，将园林树木分为林木类、花木类、果木类和叶木类。当按照各种不同的分科规则，还可以将花木类进行分类，将其继续分为牡丹、海棠等，**直到能够构造出一个自顶向下渐趋复杂的抽象层次结构为止。**

      然而，**在抽象过程中，由于规则的不严格性，会导致抽象面临着挑战。**例如，鲸鱼可以划分在哺乳类中，但是也有标准让其划分在鱼类中。**合适的规则集合对于抽象非常重要。**

   4. **将软件重用得以保证。抽象强调实体的本质、内在的属性。**我们将这种进行特性对比，并且找到可供重用的近似抽象的过程称为模式匹配和重用。**在软件系统开发过程中，模式匹配和重用也是面向对象软件开发的重要技术之一，它避免了每做一个项目必须重新开始的麻烦。如果能够充分地利用抽象的过程，在项目实施中将获得极大的生产力。良好的抽象，再怎么着也不会过时。**

   **抽象忽略了事物中与当前目标无关的非本质特性，强调与当前事物相关的特性，并将事物正确地归类，得出事物的抽象模型，并且为对象的重用提供了保障。我们是通过类来实现对象状态和行为的抽象。**

2. 封装

   **封装（Encapsulation）就是把对象的状态和行为绑到一直的机制，使对象形成一个独立的整体，并且尽可能地隐藏对象的内部细节。**封装有两个含义：**一是把对象的全部状态和行为结合在一起，形成一个不可分割的整体。对象的私有属性只能够由对象的行为来修改和读取。二是尽可能隐藏对象的内部细节，与外界的联系只能够通过外部接口来实现。**

   **封装的信息屏蔽作用反映了事物的相对独立性，我们可以只关心它对外所提供的接口，即能够提供什么样的服务，而不用去关注其内部的细节问题。**比如说一台电脑，关注的通常是这台电脑能够干什么，而不用关注其芯片是怎样做出来的。

   **封装的结果使对象以外的部分不能随意去更改对象的内部属性或状态，如果需要更改对象内部的属性或状态，需要通过公共访问控制器来进行。**通过公共访问控制器来限制对象的私有属性，有以下好处：

   1. **避免对封装数据的未授权访问。**当对象为维护一些信息，这些信息比较重要，不能够随便向外界传递时，只需要将这些信息属性设置为私有即可。
   2. **帮助保护数据的完整性。**当对象的属性设置为公共访问的时候，代码可以不经过对象所属类希望遵循的业务流程而去修改对象的值，对象很容易失去对其数据的控制。可以通过访问控制器来修改私有属性的值，并且在赋值或取值的时候检查属性值的正确与否。
   3. **当类的私有方法必须修改时，限制了在整个应该程序内的影响。**当对象采用一个公共的属性去暴露的时候，我们知道，甚至这个公共属性的名称修改一下，这个程序都需要修改这个公共属性被调用的地方。但是通过私有的方式就能够缩小影响的范围，将程序的影响范围缩小到一个类中。

   但是在实际项目中，一味地强调封装，对象的任何属性都不允许外部直接读取，反而会增加许多无意义的操作，为编程增加负担。为避免这一点，**在语言的具体使用过程中，应该根据需要，和具体情况相符合，来决定对象属性的可见性。**

3. 继承

   **对于客观事物的认知，既应该看到其共性，也应该看到其特性。**

   如果只考虑事物的共性，不考虑事物的特性，就不能反映出客观世界中事物之间的层次关系，从而不能完整、正确地对客观世界进行抽象的描述。**如果说运用抽象的原则就是舍弃对象的特性，提取其共性，从而得到适合一个对象集的类的话，那么在这个类的基础上，再重新考虑抽象过程中被舍弃的那一部分对象的特性，则可以形成一个新的类，这个类具有前一个类的全部特征，是前一个类的子集，从而形成一种层次结构，即继承结构。**

   **继承（Inheritance）是一种连接类与类之间的层次模型，是指特殊类的对象拥有其一般类的属性和行为。特殊类中不必重新对已经在一般类中所定义过的属性和行为进行定义。特殊类自动地、隐含地拥有其一般类的属性和行为。**

   **继承对类的重用性提供了一种明确表述共性的方法，即一个特殊类既有自己定义的属性和行为，又有继承下来的属性和行为。尽管继承下来的属性和行为在特殊类中是隐式的，但无论在概念上还是实际效果上，都是这个类的属性和行为。继承是传递的，当这个特殊类被它更下层的特殊类继承时，它继承来的与自己定义的属性和行为又被下一层的特殊类继承下去。有时把一般类称为基类，把特殊类称为派生类。**

   继承在面向对象软件开发过程中有关很重要的作用：

   1. **派生类只需要描述那些与基类不同的地方，把这些添加到类中然后继承即可。**不需要将基类的属性和行为再全部描述一遍。
   2. **能够重用和扩展现有类库资源。**当使用已经封装好的类库时，如果需要对某个类进行扩展，通过继承的方式很容易实现，需要不需要再去重新编写实现，并且扩展一个类的时候并不需要其源代码。
   3. **使软件易于维护和修改。**当要修改或增加某一属性或行为时，只需要在相应的类中进行改动，而它的派生的所有类全都自动地、隐含地做了相应的修改。

   **在软件开发过程中，继承性实现了软件模块的可重用性、独立性，缩短了开发的周期，提高了软件的开发效率，同时使软件易于维护和修改。**

4. 多态

   **多态是指两个或多个属于不同类的对象，对于同一个消息或方法调用所做出不同响应的能力。面向对象设计也借鉴了客观世界的多态性，体现在不同的对象可以根据相同的消息产生各自不同的动作。**例如，在“动物”基类中定义了“叫”这个行为，但并不指定这个行为在执行时叫出什么样的声音。派生类“狗”和“猫”都继承了动物类的叫的行为，但其叫的声音却不同。**这样一个叫的消息发出以后，猫类和狗类的对象根据接收到这个消息后各自执行不同叫声。这就是多态性的表现。**

   **具体到面向对象程序设计来讲，多态性（Polymorphinsm）是指在两个或多个属于不同类中同一函数名对应多个具有相似功能的不同函数，可以使用相同的调用方式来调用这些具有不同功能的同名函数。**

   **继承性和多态性的结合，可以生成一系列虽然类似但又独一无二的对象。由于继承性，这些对象共享许多相似的特征；由于多态性，针对相同的消息，不同对象可以有独特的表现方式，实现个性化的设计。**

   **上述面向对象技术的几个特征的运用，对提高软件的开发效率起着非常重要的作用，通过编写可重用的代码、编写可维护的代码，修改代码模块、共享代码等方法充分发挥其优势。**

## 什么是模型

**模型就是对现实客观世界的形状或状态的抽象模拟和简化。模型提供了系统的骨架（Sketch）和蓝图（Blueprint）。模型给人们展示系统的各个部分是如何组织起来的，模型既可以包括详细的计划，也可以包括从很高的层次考虑系统的总体计划。一个好的模型包括那些有广泛影响的主要元素，而忽略那些与给定的抽象水平不相关的次要元素。每个系统都可以从不同的方面用不同的模型来描述，因而每个模型都是一个在语义上闭合的系统抽象。模型可以是结构性的，强调系统的组织，也可以是行为性的，强调系统的动态方面。对象建模的目标就是要为正在开发的系统制定一个精确、简明和易理解的面向对象模型。**

### 为什么要建模

使用模型建模不仅仅适用于建筑行业。

**建模是为了能够更好地理解正在开发的系统。**那么具体到软件所涉及的人员，包括系统用户、软件开发团队、软件的维护和技术支持者，系统建模都有什么样的作用呢？

1. **对于软件系统用户，软件的开发模型向他们描述了软件开发者对于软件系统需求的理解。**让系统用户查看软件对象模型并且找到其中的问题，这样可以使用户开发者不至于从一开始就发生错误。能够很大程度地节约成本。
2. **对于软件开发团队，软件的对象模型有助于帮助他们对软件的需求以及系统的架构和功能进行沟通。**需求和架构的一致理解对于软件开发团队是非常重要的，可以减少不必要的麻烦。软件对象建模的受益者不仅仅包括代码的编写者，还包括软件的测试者和文档的编写者。
3. **对于软件的维护和技术支持者，在软件系统开始运行后的相当长的一段时间内，软件的对象模型能够帮助他们理解程序的架构和功能，迅速地对软件所出现的问题进行修复。**

建模并不仅仅针对的是大型的软件系统，甚至一个小型的电话簿软件也能从建模过程中受益。事实上，**系统越大、越复杂，建模的重要性就越大。**一个很简单的原因就是：**人对复杂问题的理解能力是有限的，人们往往不能完整地理解一个复杂的系统，所以要对它建模。**

**通过建模，可以缩小所研究问题的范围，一次只需要重点研究它的一个很小的方面，这就是“分而治之”的策略方法，即把一个困难问题划分成一系列能够解决的小问题，对这些小问题的解决也就构成对复杂问题的解决。一个适当选择的模型可以使建模人员在较高的抽象层次上工作。**

### 建模的目标和原则

**建立模型可以帮助开发者更好地了解正在开发的系统。**通过建模，要实现以下四个目标：

1. 便于开发人员展现系统。
2. 允许开发人员制定系统的结构或行为。
3. 提供指导开发人员构造系统的模板。
4. 记录开发人员的决策。

在工程学科中，对模型的使用有着悠久的历史，人们从中总结出了四条基本的建模原则：

1. **选择要创建什么模型，对如何动手解决问题和如何形成解决方案有着意义深远的影响。**换句话说，就是要认真地选择模型。

2. **可以在不同的精度级别上表示每一种模型。**如果正在建造一座大厦，有时需要从宏观上让投资者看到大厦的样子，感觉到大厦的总体效果。而有时又需要认真考虑细节问题，例如，对复杂管道的铺设，或对少见的结构件的安装等。无论如何，使用者的身份和使用的原因是评判模型优劣的关键。**分析者和最终的用户关心“是什么”，而开发者关心“如何实现”。所有的参与者都想在不同的时期、从不同的角度了解系统。**

3. 最好的模型是与现实相联系的。如果只假定了理想条件和完美制造，则可能掩盖真实的一些潜在的、致命的现实特征。**最好是有能够清晰地联系实际的模型，而当联系很薄弱时能够精确地知道这些模型怎样与现实脱节。所有的模型都对现实进行了简化。但有一点要记住，关键是简化不要掩盖掉任何重要的细节。**

4. **孤立的模型是不完整的。每个重要的系统都是由多个几乎独立的模型组合出来的。**

   **在任何种类的模型中都需要从多视角来把握系统的范围（如不同楼层的蓝图）。既能够单独地研究电气设计图，也能看到它如何映射到楼层平面图中，以及它与管道设计图中的管子排布的相互影响。**

## 用面向对象设计项目

**用面向对象设计项目就是从不稳定的需求中分析出稳定的对象，以对象为基础来组织需求、构架系统。这种方法包括了面向对象分析和面向对象设计。**

### 面向对象分析

**面向对象分析的目的是认知客观世界的系统并对系统进行建模。那么就需要在面向对象分析过程中根据客观世界的具体实例来建立准确、具体、严密的分析模型。**构造分析模型的用途有三种：

1. 明确问题域的需求。
2. 为用户和开发人员提供明确需求。
3. 为用户和开发人员提供一个协商的基础，作为后继的设计和实现的框架。需求分析的结果应以文档的形式存在。

**面向对象的具体分析过程包括了获取需求内容陈述、建立系统的对象模型结构、建立对象的动态模型、建立系统功能建模和确定类的操作5个步骤。**

#### 获取需求内容陈述

**系统分析的第一步就是获取需求内容陈述。分析者必须与用户一块工作来提炼这些需求，必须搞清楚用户的真实意图是什么，其中的过程涉及对需求的分析及关联信息的查找。**

#### 建立系统的对象模型结构

**系统分析的第二步就是建立系统的对象模型结构。**

**要建立系统的对象模型结构首先需要标识和关联类，因为类的确定和关联影响了整个系统的结构和解决问题的方法。其次是增加类的属性，进一步描述类和关联的基本网络，在这个过程中可以使用继承、包等来组织类。最后是将操作增加到类中去作为构造动态模型和功能模型的副产品。下面分别进行介绍：**

1. **标识和确定类。构造对象模型的第一步是标出来自问题域的相关对象类，这些对象类包括物理实体和概念的描述。**所有类在应用中都应当是有意义的，在问题陈述中，并非所有类都是明显给出的。有些是隐含在问题域或一般知识中的。通常来说，**一个确定类的过程包括，从需求说明中选取相关的名词，确定一些类，然后对这些类进行分析，过滤掉不符合条件的类。**

   ` 需求说明->选取相关名词->暂定类->过滤不符合类->类

   **查找问题陈述中的所有名词，产生暂定类。**

   接下来根据下列标准，去年一些不必要的类和不正确的类。

   - **消除冗余类。**如果存在两个类表述了同一个信息，则保留最富有描述能力并且和系统紧密相关的类。如“外借物料者”和“部门经理”就是重复的描述，因为“外借物料者”最富有描述性，因此保留它。
   - **去除掉与系统不相干的类。**与问题没有关系或根本无关的类，在类的确定中应当去除掉。例如。打扫仓库的卫生超出了仓库管理信息系统的范围。
   - **去除掉模糊类。**由于类必须是确定和明确的，有些暂定类中边界的定义模糊或范围太广，如“软件”和“员工代理”就是模糊类，就这个系统而言，它是指“仓库管理信息系统”。
   - **去除掉属性**。某些名词描述的是其他对象的属性，应当把这些类从暂定类中删除掉。**但是如果某一个名词的独立性很重要，就应该把它归属到类，而不把它作为属性**。如“领取物料的名称”和“领取物料的编号”属于物料信息的发生，应当去除。
   - **去除操作。**如果问题陈述的名词中有动作含义的名词，则含有这样描述的操作的名词就不应当是类。**但是具有自身性质且需要独立存在的操作应该描述成类。**

   在仓库管理信息系统中，根据上面的标准，把“软件”、“员工代理”、“领取物料的名称”、“领取物料的编号”、“部门经理”和“普通员工”等这些类除去。

2. **准备数据字典。为所有建模实体准备一个数据字典来进行描述。**数据字典应当准确描述各个类的精确含义，描述当前问题中类的范围，包括对类的成员、用法方面的假设或限制。例如，物料信息应当包括物料的名称、物料的编号、物料的分类、物料入库时间、物料出库时间、物料的供应商等。

3. **确定关联。关联是指两个或多个类之间的相互依赖关系。一种依赖表示一种关联，可用各种方式来实现关联，但在分析模型中应删除实现的考虑，以便设计时更为灵活。关联常用描述性动词或动词词组来表示，其中有物理位置的表示、传导的动作、通信、所有者关系、条件的满足等。从问题陈述中抽取所有可能的关联表述，把它们记下来，但不要过早去细化这些表述。**

   **系统中所有可能的关联，大多数是直接抽取问题中的动词词组而得到的。在陈述中，有些动词词组表述的关联是不明显的。最后，还有一些关联与客观世界或人的假设有关，必须同用户一直核实这种关联，因为这种关联在问题陈述中找不到。**

   仓库管理信息系统问题陈述中的关联：

   - 每个可借取物料的员工建立一个账号
   - 账号可以提供该类员工的工号、姓名和所属部门
   - 账号中存储该类员工的个人信息，借取物料以及预约的信息
   - 拥有账号的员工才能借取物料、预约物料并取消预约
   - 。。。

4. **确定属性。属性是个体对象的性质，属性通常用修饰性的名词词组来表示。形容词常常表示具体的可枚举的属性值，属性不可能在问题陈述中完全表述出来，必须借助于应用域的知识及对客观世界的知识才可以找到它们。只考虑与具体应用直接相关的属性，不要考虑那些走出问题范围的属性。首先找出重要属性，避免那些只用于实现的属性，要为各个属性取有意义的名字。**

5. **使用继承来细化类。使用继承来共享公共属性，依此来对类进行组织，一般可以使用下列两种方式来进行：**

   - **自底向上通过把现有类的共同性质一般化为父类，寻找具有相似的属性、关系或操作的类来发现继承。**例如，“本科生”和“大专生”是类似的，可以一般化为“大学生”。这些一般化结果常常是基于客观世界的现有分类，**只要可能，尽量使用现有概念。**
   - **自顶向下将现有的类细化为更具体的子类。具体化常常可以从应用域中明显看出来。在应用域中各枚举情况是最常见的具体化的来源。**例如，菜单可以有固定菜单、顶部菜单、弹出菜单、下拉菜单等，这就可以把菜单类具体细化为各种具体菜单的子类。**当同一关联名出现多次且意义也相同时，应尽量具体化为相关联的类。在类层次中，可以为具体的类来分配属性和关联。各属性和关联都应分配给最一般的适合的类，有时也加上一些修正。应用域中各枚举情况是最常见的具体化的来源。**

6. **完善对象模型。对象建模不可能一次就能保证模型是完全正确的，软件开发的整个过程就是一个不断完善的过程。模型的不同组成部分多半是在不同的阶段完成的，如果发现模型的缺陷，就必须返回到前期阶段去修改，有些细化工作是在动态模型和功能模型完成之后才开始进行的。**

#### 建立对象的动态模型

**进行分析的第三步是建立对象的动态模型。建立对象的动态模型一般包含下列几个步骤：**

1. 准备脚本。动态分析从寻找事件开始，然后确定各对象的可能事件顺序。
2. 确定事件。确定所有外部事件。事件包括所有来自或发往用户的信息、外部设备的信号、输入、转换和动作，可以发现正常事件，但不能遗漏条件和异常事件
3. 准备事件跟踪表。把脚本表示成一个事件跟踪表，即不同对象之间的事件排序表，对象为表中的列，给每个对象分配一个独立的列。
4. 构造状态图。对各对象类建立状态图，反映对象接收和发送的事件，每个事件跟踪都对应于状态图中一条路径。

#### 建立系统功能建模

**进行分析的第四步是建立对象的功能模型。功能模型用来说明值是如何计算的，标明值与值之间的依赖关系及相关的功能。数据流图有助于表示功能依赖关系，其中的处理在状态图的活动和动作进行标识，其中的数据流对应于对象图中的对象或属性。**

1. 确定输入、输出值：先列出输入、输出值，输入、输出值是系统与外界之间的事件的参数。
2. 建立数据流图：数据流图说明输出值是怎样从输入值得来的，数据流图通常按层次组织。

#### 确定类的操作

**在建立对象模型时，确定了类、关联、结构和属性，还没有确定操作。只有建立了动态模型和功能模型之后，才可能最后确定类的操作。**

### 面向对象设计

**面向对象设计是把分析阶段得到的需求转变成符合成本和质量要求的、抽象的系统实现方案的过程。从面向对象分析到面向对象设计，是一个逐渐扩充模型的过程。**

**系统设计确定实现系统的策略和目标系统的高层结构。对象设计确定问题空间中的类、关联、接口形式及实现操作的算法。**

#### 面向对象设计的准则

**面向对象设计的准则包括模块化、抽象、信息隐藏、低耦合和高内聚等特征。**下面对这些特征进行介绍：

1. **模块化。面向对象开发方法很自然地支持了把系统分解成模块的设计原则——对象就是模块。它是把数据结构和操作这些数据的方法紧密地结合在一起所构成的模块。**类的设计要很好地支持模块化这一准则，这样使系统能够有更好的维护性。
2. **抽象。面向对象方法不仅支持对过程进行抽象，而且支持对数据进行抽象。**抽象方法的好坏以及抽象的层次都对系统的设计有很大影响。
3. **信息隐藏。**在面向对象方法中，信息隐藏是通过对象的封装性来进行实现对象暴露接口的多少以及接口的好坏都对系统设计有很大影响。
4. **低耦合。**在面向对象方法中，对象是最基本的模块，因此，耦合主要指不同对象之间相互关联的紧密程度。低耦合是设计的一个重要标准，因为这有助于使得系统中某一部分的变化对其他部分的影响降到最低程度。
5. **高内聚。**在面向对象方法中，高内聚也是必须进行满足的条件。高内聚是指在一个对象类中应尽量多地洪逻辑上相关的计算资源。如果一个模块只负责一件事情，就说明这个模块有很高的内聚度；如果一个模块负责了很多毫不相关的事情，则说明这个模块的内聚度很低。内聚度高的模块通常很容易理解，很容易被复用、扩展和维护。

#### 面向对象设计的启发规则

**在面向对象设计中，可以通过使用一些实用的规则来指导我们进行面向对象的设计。通常这些面向对象设计的启发规则包含以下内容：

1. **设计的结果应该清晰易懂。**使设计结果清晰、易懂、易读是提高软件可维护性和可重用性的重要措施。显然，人们不会重用那些他们不理解的设计。
2. **一般到具体结构的尝试应该适当。**通常来说，**从一般到具体的抽象过程，抽象的越深，对于程序的可移植性也就越好，但是抽象层次的过多会给编写和维护带来很大的麻烦。**一般来说，**适度的抽象能够更好地提高软件的开发效率和维护工作。**具体的情况需要系统分析员根据具体的情况进行抽象。
3. **尽量设计小而简单的类。系统设计应当尽量去设计小而简单的类，这样便于程序的开发和管理。**
4. **使用简单的消息协议。**简单的消息协议有助于帮助记忆和测试。一般来讲，消息中的参数个数不要越过3个。
5. **使用简单的函数或方法。面向对象设计出来的类中的函数或方法通常来讲要尽可能地小，一般只有3～5行源程序即可。**
6. **把设计变动减至最小。通常，设计的质量越高，设计结果保持不变的时间也越长。即使出现必须修改设计的情况，也应该使修改的范围尽可能小。**

#### 系统设计

**系统设计是问题求解及建立解答的高级策略。必须制定解决问题的基本方法，系统的高层结构形式包括子系统的分解、它的固有并发性、子系统分配给硬软件、数据存储管理、资源协调、软件控制实现、人机交互接口等。**

**系统设计一般是先从高层入手，然后细化。系统设计要决定整个结构及风格，这种结构为后面设计阶段的更详细策略的设计提供了基础。**下面显示了整个系统设计的一般步骤。

1. 系统分解。系统中主要的组成部分称为子系统，子系统既不是一个对象也不是一个功能，而是类、关联、操作、事件和约束的集合。
2. 确定并发性。分析模型、现实世界及硬件中不少对象均是并发的。
3. 处理器及任务分配。各并发子系统必须分配给单个硬件单元，要么是一个一般的处理器，要么是一个具体的功能单元。
4. 数据存储管理。通常各数据存储可以将数据结构、文件、数据库组合在一起，不同数据存储要在费用、访问时间、容量及可靠性之间做出折中考虑。
5. 全局资源的处理。必须确定全局资源，并且制定访问全局资源的策略。
6. 选择软件控制机制。系统设计必须从多种方法中选择某种方法来实现软件的控制。
7. 人机交互接口设计。设计中的大部分工作都与稳定的状态行为有关，但必须考虑用户使用系统的交互接口。

## 什么是UML

模型种类

1. 瀑布模型

2. 喷泉模型

3. 基于构件的开发模型

4. XP方法

   **敏捷方法是近几年兴起的一种轻量级的开发方法，它规定了一组核心价值和方法，消除了大多数重量型开发过程中的不必须产物，建立了一个渐进型开发过程。**该方法将开发阶段的四个活动（分析、设计、编码和测试）混合在一起，在全过程中采用迭代增量开发、反馈修正和反复测试。它把软件生命周期划分为用户场景、系统架构、发布计划、迭代、验证测试和小型发布6个阶段。采用这种开发模型的软件开发过程。

XP模型通过对传统软件开发的标准方法进行重新审视，提出了由一组规则组成的一些简便易行的过程。由于这些规则是通过在实践中观察使软件高效或缓慢的因素而得出的，因此，**它既考虑了保持开发人员的活力和创造性，又考虑了开发过程的有组织、有重点和持续性。XP模型是面向客户的开发模型，重点强调用户的满意程度。开发过程中对需求改变的适应能力较高**，即使在开发的后期，也可较高程度地适应用户的改变。

XP开发模型与传统模型相比具有很大的不同，其**核心思想是交流（Communication）、简单（Simplicity）、反馈（Feedback）和进取（Aggressiveness）。**XP开发小组不仅包括开发人员，还包括管理人员和客户。该模型强调小组内成员之间要经常进行交流，在尽量保证质量可以运行的前提下力求过程和代码的简单化；来自客户、开发人员和最终用户的具体反馈意见可以提供更多的机会来调整设计，保证把握正确的开发方向；进取则包含于上述3个原则中。

XP开发方法中有许多新思路，如采用“用户场景”代替传统模型中的需求分析，“用户场景”由用户用自己领域中的词汇并且不考虑任何技术细节准确地表达自己的需求。XP模型的优点如下：

1. 采用简单计划策略，不需要长期计划和复杂模型，开发周期短。
2. 在全过程采用迭代增量开发、反馈修正和反复测试的方法，软件质量有保证。
3. 能够适应用户经常变化的需求，提供用户满意的高质量软件。

上面的开发模型方法或许不能一概而论说是面向对象的建模为基础的开发模式，但是在各种开发方法中，都包含了软件的需求分析、软件的设计、软件的开发、软件的测试和软件的部署。在每一个阶段，可以借助于面向对象的建模和这些开发模型形成一套适合自己或企业的开发方式。主要体现在：

1. 软件的需求分析阶段，对系统将要面临的具体管理问题以及用户对系统开发的需求进行调查研究，即先弄清要干什么的问题。然后分析问题的性质和求解问题，在繁杂的问题域中抽象地识别出对象以及其行为、结构、属性、方法等。一般称之为面向对象的分析，即OOA。
2. 软件的设计阶段，整理问题，对分析的结果做进一步的抽象、归类、整理，并最终以范式的形式将它们确定下来。一般称之为面向对象的设计，即OOD。
3. 软件的开发阶段，也即程序实现阶段，用面向对象的程序设计语言将上一步整理的范式直接映射（即直接用程序设计语言来取代）为应用软件。一般称之为面向对象的程序，即OOP。

开发模式或方法毕竟是方法，如同在冷兵器时代的排兵布阵和火器时代的排兵布阵一样，都有自己的技巧和内容，但是，由于一个是面向过程，一个是面向对象的不同而赋予了不同的内容。在这些开发模型中，对于适用UML和面向对象开发的代表Rational统一过程（Rational Unified Process，RUP），在第3章将会详细讲解。
