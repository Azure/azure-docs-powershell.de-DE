---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005859"
---
# <span data-ttu-id="a86d8-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a86d8-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="a86d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a86d8-102">SYNOPSIS</span></span>

<span data-ttu-id="a86d8-103">Ruft eine Automatisierungs Variable ab.</span><span class="sxs-lookup"><span data-stu-id="a86d8-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="a86d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a86d8-104">SYNTAX</span></span>

### <span data-ttu-id="a86d8-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="a86d8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a86d8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a86d8-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a86d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a86d8-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a86d8-108">Das Cmdlet " **Get-AzureAutomationVariable** " ruft mindestens eine Microsoft Azure-Automatisierungs Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="a86d8-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="a86d8-109">Standardmäßig werden alle Variablen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a86d8-109">By default, all variables are returned.</span></span>
<span data-ttu-id="a86d8-110">Um eine bestimmte Variable abzurufen, geben Sie Ihren Namen ein.</span><span class="sxs-lookup"><span data-stu-id="a86d8-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="a86d8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a86d8-111">EXAMPLES</span></span>

### <span data-ttu-id="a86d8-112">Beispiel 1: Abrufen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="a86d8-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="a86d8-113">Diese Befehle rufen eine Automatisierungs Variable mit dem Namen myVariable ab und weisen deren Wert einer Variablen mit dem Namen $Value zu.</span><span class="sxs-lookup"><span data-stu-id="a86d8-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="a86d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a86d8-114">PARAMETERS</span></span>

### <span data-ttu-id="a86d8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a86d8-115">-AutomationAccountName</span></span>
<span data-ttu-id="a86d8-116">Gibt den Namen des Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a86d8-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="a86d8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a86d8-117">-Name</span></span>
<span data-ttu-id="a86d8-118">Gibt den Namen einer Variablen an.</span><span class="sxs-lookup"><span data-stu-id="a86d8-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86d8-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="a86d8-119">-Profile</span></span>
<span data-ttu-id="a86d8-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a86d8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a86d8-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a86d8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a86d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86d8-122">CommonParameters</span></span>
<span data-ttu-id="a86d8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86d8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86d8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86d8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a86d8-125">INPUTS</span></span>

## <span data-ttu-id="a86d8-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a86d8-126">OUTPUTS</span></span>

### <span data-ttu-id="a86d8-127">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="a86d8-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a86d8-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a86d8-128">NOTES</span></span>

## <span data-ttu-id="a86d8-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a86d8-129">RELATED LINKS</span></span>

[<span data-ttu-id="a86d8-130">Neu – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a86d8-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="a86d8-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a86d8-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="a86d8-132">Satz-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a86d8-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


