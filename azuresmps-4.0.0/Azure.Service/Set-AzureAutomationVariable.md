---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006274"
---
# <span data-ttu-id="1859a-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1859a-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="1859a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1859a-102">SYNOPSIS</span></span>

<span data-ttu-id="1859a-103">Ändert eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="1859a-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="1859a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1859a-104">SYNTAX</span></span>

### <span data-ttu-id="1859a-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="1859a-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1859a-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="1859a-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1859a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1859a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1859a-108">Das Cmdlet " **Satz-AzureAutomationVariable** " ändert den Wert oder die Beschreibung einer Variablen in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="1859a-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1859a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1859a-109">EXAMPLES</span></span>

### <span data-ttu-id="1859a-110">Beispiel 1: Setzen des Werts einer Variablen</span><span class="sxs-lookup"><span data-stu-id="1859a-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="1859a-111">Mit diesem Befehl wird ein neuer Wert für die Variable mit dem Namen MyStringVariable im Azure-Automatisierungs Konto mit dem Namen Contoso17 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1859a-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1859a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1859a-112">PARAMETERS</span></span>

### <span data-ttu-id="1859a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1859a-113">-AutomationAccountName</span></span>
<span data-ttu-id="1859a-114">Gibt den Namen des Automatisierungs Kontos mit der Variablen an.</span><span class="sxs-lookup"><span data-stu-id="1859a-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="1859a-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1859a-115">-Description</span></span>
<span data-ttu-id="1859a-116">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="1859a-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1859a-117">-Verschlüsselt</span><span class="sxs-lookup"><span data-stu-id="1859a-117">-Encrypted</span></span>
<span data-ttu-id="1859a-118">Gibt an, ob die Variable verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1859a-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1859a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1859a-119">-Name</span></span>
<span data-ttu-id="1859a-120">Gibt den Namen der Variablen an.</span><span class="sxs-lookup"><span data-stu-id="1859a-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="1859a-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="1859a-121">-Profile</span></span>
<span data-ttu-id="1859a-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1859a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1859a-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1859a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1859a-124">-Wert</span><span class="sxs-lookup"><span data-stu-id="1859a-124">-Value</span></span>
<span data-ttu-id="1859a-125">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="1859a-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1859a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1859a-126">CommonParameters</span></span>
<span data-ttu-id="1859a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1859a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1859a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1859a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1859a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1859a-129">INPUTS</span></span>

## <span data-ttu-id="1859a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1859a-130">OUTPUTS</span></span>

### <span data-ttu-id="1859a-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="1859a-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1859a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1859a-132">NOTES</span></span>

## <span data-ttu-id="1859a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1859a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1859a-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1859a-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="1859a-135">Neu – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1859a-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="1859a-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1859a-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


