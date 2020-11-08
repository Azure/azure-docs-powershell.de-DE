---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006140"
---
# <span data-ttu-id="a8976-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="a8976-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8976-102">SYNOPSIS</span></span>

<span data-ttu-id="a8976-103">Erstellt eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8976-103">Creates a runbook.</span></span>

## <span data-ttu-id="a8976-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8976-104">SYNTAX</span></span>

### <span data-ttu-id="a8976-105">ByRunbookName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8976-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a8976-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="a8976-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8976-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8976-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a8976-108">Das Cmdlet **New-AzureAutomationRunbook** erstellt eine neue, leere Microsoft Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8976-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="a8976-109">Geben Sie einen Namen ein, um einen neuen runbooks zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8976-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="a8976-110">Sie können auch den Pfad zu einer Windows PowerShell-Skriptdatei (ps1) angeben, um eine runbooks zu importieren.</span><span class="sxs-lookup"><span data-stu-id="a8976-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="a8976-111">Das zu importierende Skript muss eine einzelne Windows PowerShell-Workflow Definition enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8976-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="a8976-112">Der Name dieses Windows PowerShell-Workflows wird zum Namen des runbooks.</span><span class="sxs-lookup"><span data-stu-id="a8976-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="a8976-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8976-113">EXAMPLES</span></span>

### <span data-ttu-id="a8976-114">Beispiel 1: Erstellen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="a8976-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="a8976-115">Dieser Befehl erstellt einen neuen runbooks mit dem Namen Runbook02 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a8976-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a8976-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8976-116">PARAMETERS</span></span>

### <span data-ttu-id="a8976-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8976-117">-AutomationAccountName</span></span>
<span data-ttu-id="a8976-118">Gibt den Namen des Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a8976-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="a8976-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8976-119">-Description</span></span>
<span data-ttu-id="a8976-120">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="a8976-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="a8976-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a8976-121">-Name</span></span>
<span data-ttu-id="a8976-122">Gibt den Namen für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="a8976-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8976-123">-Path</span><span class="sxs-lookup"><span data-stu-id="a8976-123">-Path</span></span>
<span data-ttu-id="a8976-124">Gibt den Pfad an.</span><span class="sxs-lookup"><span data-stu-id="a8976-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8976-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8976-125">-Profile</span></span>
<span data-ttu-id="a8976-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a8976-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8976-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a8976-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8976-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="a8976-128">-Tags</span></span>
<span data-ttu-id="a8976-129">Gibt Tags für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="a8976-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8976-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8976-130">CommonParameters</span></span>
<span data-ttu-id="a8976-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8976-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8976-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8976-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8976-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8976-133">INPUTS</span></span>

## <span data-ttu-id="a8976-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8976-134">OUTPUTS</span></span>

### <span data-ttu-id="a8976-135">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="a8976-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a8976-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8976-136">NOTES</span></span>

## <span data-ttu-id="a8976-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8976-137">RELATED LINKS</span></span>

[<span data-ttu-id="a8976-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="a8976-139">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="a8976-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="a8976-141">Satz-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="a8976-142">Anfang-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8976-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


