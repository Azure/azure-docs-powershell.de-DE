---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471392"
---
# <span data-ttu-id="cb9a0-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cb9a0-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="cb9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9a0-103">Exportiert den Rohinhalt eines DSC-Berichts, der von einem DSC-Knoten in die Automatisierung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="cb9a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb9a0-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb9a0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9a0-106">Das **Cmdlet "Export-AzAutomationDscNodeReportContent"** exportiert den Rohinhalt eines BERICHTS "APS Desired State Configuration (DSC)".</span><span class="sxs-lookup"><span data-stu-id="cb9a0-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="cb9a0-107">Ein DSC-Knoten sendet einen DSC-Bericht an die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="cb9a0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb9a0-108">EXAMPLES</span></span>

### <span data-ttu-id="cb9a0-109">Beispiel 1: Exportieren eines Berichts aus einem DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="cb9a0-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="cb9a0-110">Diese Gruppe von Befehlen exportiert den neuesten Bericht aus dem KNOTEN "DSC" namens "Computer14" auf den Desktop.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="cb9a0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9a0-111">PARAMETERS</span></span>

### <span data-ttu-id="cb9a0-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb9a0-112">-AutomationAccountName</span></span>
<span data-ttu-id="cb9a0-113">Gibt den Namen eines Automatisierungskontos an.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="cb9a0-114">Dieses Cmdlet exportiert Berichtsinhalte für einen DSC-Knoten, der zu dem Automatisierungskonto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9a0-115">-DefaultProfile</span></span>
<span data-ttu-id="cb9a0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cb9a0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cb9a0-117">-Force</span></span>
<span data-ttu-id="cb9a0-118">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei mit demselben Namen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="cb9a0-119">-NodeId</span></span>
<span data-ttu-id="cb9a0-120">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="cb9a0-121">-OutputFolder</span></span>
<span data-ttu-id="cb9a0-122">Gibt den Ausgabeordner an, in den dieses Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="cb9a0-123">-ReportId</span></span>
<span data-ttu-id="cb9a0-124">Gibt die eindeutige ID des DSC-Knotenberichts an, den dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb9a0-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cb9a0-127">Dieses Cmdlet exportiert den Inhalt eines Berichts für den DSC-Knoten, der zu der Von diesem Cmdlet angegebenen Ressourcengruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb9a0-128">-Confirm</span></span>
<span data-ttu-id="cb9a0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cb9a0-130">-WhatIf</span></span>
<span data-ttu-id="cb9a0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9a0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9a0-133">CommonParameters</span></span>
<span data-ttu-id="cb9a0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9a0-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9a0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9a0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb9a0-136">INPUTS</span></span>

### <span data-ttu-id="cb9a0-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cb9a0-137">System.Guid</span></span>

### <span data-ttu-id="cb9a0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cb9a0-138">System.String</span></span>

## <span data-ttu-id="cb9a0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb9a0-139">OUTPUTS</span></span>

### <span data-ttu-id="cb9a0-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="cb9a0-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="cb9a0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb9a0-141">NOTES</span></span>

## <span data-ttu-id="cb9a0-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb9a0-142">RELATED LINKS</span></span>

[<span data-ttu-id="cb9a0-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cb9a0-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="cb9a0-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cb9a0-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cb9a0-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="cb9a0-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


