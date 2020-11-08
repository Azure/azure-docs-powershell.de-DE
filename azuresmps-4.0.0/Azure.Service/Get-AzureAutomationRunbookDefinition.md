---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006568"
---
# <span data-ttu-id="52ec9-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="52ec9-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="52ec9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52ec9-102">SYNOPSIS</span></span>

<span data-ttu-id="52ec9-103">Ruft eine runbooks-Definition ab.</span><span class="sxs-lookup"><span data-stu-id="52ec9-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="52ec9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52ec9-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52ec9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52ec9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="52ec9-106">Das Cmdlet " **Get-AzureAutomationRunbookDefinition** " Ruft die Entwurfsdefinition, die veröffentlichte Definition oder beide Definitionen eines Azure Automation-runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="52ec9-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="52ec9-107">Standardmäßig wird die veröffentlichte Version zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52ec9-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="52ec9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52ec9-108">EXAMPLES</span></span>

### <span data-ttu-id="52ec9-109">Beispiel 1: Abrufen einer runbooks-Definition</span><span class="sxs-lookup"><span data-stu-id="52ec9-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="52ec9-110">Dieser Befehl ruft die veröffentlichte runbooks-Definition des runbooks mit dem Namen RunbookDef01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="52ec9-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="52ec9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="52ec9-111">PARAMETERS</span></span>

### <span data-ttu-id="52ec9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52ec9-112">-AutomationAccountName</span></span>
<span data-ttu-id="52ec9-113">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="52ec9-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="52ec9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="52ec9-114">-Name</span></span>
<span data-ttu-id="52ec9-115">Gibt den Namen einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="52ec9-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ec9-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="52ec9-116">-Profile</span></span>
<span data-ttu-id="52ec9-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="52ec9-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52ec9-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="52ec9-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52ec9-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="52ec9-119">-Slot</span></span>
<span data-ttu-id="52ec9-120">Gibt den Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="52ec9-120">Specifies the slot.</span></span>
<span data-ttu-id="52ec9-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="52ec9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52ec9-122">Entwurf</span><span class="sxs-lookup"><span data-stu-id="52ec9-122">Draft</span></span>
- <span data-ttu-id="52ec9-123">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="52ec9-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ec9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ec9-124">CommonParameters</span></span>
<span data-ttu-id="52ec9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ec9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ec9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ec9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ec9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52ec9-127">INPUTS</span></span>

## <span data-ttu-id="52ec9-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52ec9-128">OUTPUTS</span></span>

## <span data-ttu-id="52ec9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="52ec9-129">NOTES</span></span>

## <span data-ttu-id="52ec9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52ec9-130">RELATED LINKS</span></span>

[<span data-ttu-id="52ec9-131">Satz-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="52ec9-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


