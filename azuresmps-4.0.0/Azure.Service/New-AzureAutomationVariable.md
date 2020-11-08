---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006137"
---
# <span data-ttu-id="f3feb-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3feb-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="f3feb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3feb-102">SYNOPSIS</span></span>

<span data-ttu-id="f3feb-103">Erstellt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="f3feb-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="f3feb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3feb-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3feb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3feb-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f3feb-106">Das Cmdlet **New-AzureAutomationVariable** erstellt eine Variable in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="f3feb-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="f3feb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3feb-107">EXAMPLES</span></span>

### <span data-ttu-id="f3feb-108">Beispiel 1: Erstellen einer neuen Variablen mit einem einfachen Wert</span><span class="sxs-lookup"><span data-stu-id="f3feb-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="f3feb-109">Dieser Befehl erstellt eine neue Variable mit dem Namen MyStringVariable mit einem Zeichenfolgenwert im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f3feb-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3feb-110">Beispiel 2: Erstellen einer neuen Variablen mit einem komplexen Wert</span><span class="sxs-lookup"><span data-stu-id="f3feb-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="f3feb-111">Diese Befehle erstellen eine neue Variable namens MyComplexVariable im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f3feb-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f3feb-112">Ein komplexes Objekt wird für seinen Wert verwendet, in diesem Fall für ein Objekt eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f3feb-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="f3feb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3feb-113">PARAMETERS</span></span>

### <span data-ttu-id="f3feb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3feb-114">-AutomationAccountName</span></span>
<span data-ttu-id="f3feb-115">Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3feb-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3feb-116">-Description</span></span>
<span data-ttu-id="f3feb-117">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="f3feb-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-118">-Verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="f3feb-118">-Encrypted</span></span>
<span data-ttu-id="f3feb-119">Gibt an, ob der Wert der Variablen verschlüsselt gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3feb-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3feb-120">-Name</span></span>
<span data-ttu-id="f3feb-121">Gibt einen Namen für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="f3feb-121">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3feb-122">-Profile</span></span>
<span data-ttu-id="f3feb-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f3feb-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3feb-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f3feb-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="f3feb-125">-Value</span></span>
<span data-ttu-id="f3feb-126">Gibt einen Wert an, der in der Variablen gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3feb-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3feb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3feb-127">CommonParameters</span></span>
<span data-ttu-id="f3feb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3feb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3feb-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3feb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3feb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3feb-130">INPUTS</span></span>

## <span data-ttu-id="f3feb-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3feb-131">OUTPUTS</span></span>

### <span data-ttu-id="f3feb-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="f3feb-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f3feb-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3feb-133">NOTES</span></span>

## <span data-ttu-id="f3feb-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3feb-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3feb-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3feb-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="f3feb-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3feb-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="f3feb-137">Satz-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f3feb-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


