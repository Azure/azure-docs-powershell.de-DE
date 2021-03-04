---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: c4006c13130cecb27c35d466c43cfd75583644b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930411"
---
# <span data-ttu-id="ac701-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="ac701-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="ac701-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac701-102">SYNOPSIS</span></span>
<span data-ttu-id="ac701-103">Exportiert den Rohinhalt eines DSC-Berichts, der von einem DSC-Knoten gesendet wurde, in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ac701-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="ac701-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac701-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac701-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac701-105">DESCRIPTION</span></span>
<span data-ttu-id="ac701-106">Das **Cmdlet Export-AzAutomationDscNodeReportContent** exportiert den Rohinhalt eines APS Desired State Configuration (DSC)-Berichts.</span><span class="sxs-lookup"><span data-stu-id="ac701-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="ac701-107">Ein DSC-Knoten sendet einen DSC-Bericht an Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ac701-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="ac701-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac701-108">EXAMPLES</span></span>

### <span data-ttu-id="ac701-109">Beispiel 1: Exportieren eines Berichts aus einem DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="ac701-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="ac701-110">Mit dieser Gruppe von Befehlen wird der neueste Bericht vom DSC-Knoten "Computer14" auf den Desktop exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac701-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="ac701-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac701-111">PARAMETERS</span></span>

### <span data-ttu-id="ac701-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ac701-112">-AutomationAccountName</span></span>
<span data-ttu-id="ac701-113">Gibt den Namen eines Automatisierungskontos an.</span><span class="sxs-lookup"><span data-stu-id="ac701-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="ac701-114">Dieses Cmdlet exportiert Berichtsinhalte für einen DSC-Knoten, der zum automatisierungskonto gehört, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ac701-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac701-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac701-115">-DefaultProfile</span></span>
<span data-ttu-id="ac701-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ac701-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac701-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ac701-117">-Force</span></span>
<span data-ttu-id="ac701-118">Gibt an, dass dieses Cmdlet eine vorhandene lokale Datei durch eine neue Datei ersetzt, die denselben Namen hat.</span><span class="sxs-lookup"><span data-stu-id="ac701-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="ac701-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="ac701-119">-NodeId</span></span>
<span data-ttu-id="ac701-120">Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac701-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="ac701-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ac701-121">-OutputFolder</span></span>
<span data-ttu-id="ac701-122">Gibt den Ausgabeordner an, in dem dieses Cmdlet Berichtsinhalte exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac701-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="ac701-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="ac701-123">-ReportId</span></span>
<span data-ttu-id="ac701-124">Gibt die eindeutige ID des DSC-Knotenberichts an, den dieses Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac701-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="ac701-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac701-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac701-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ac701-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ac701-127">Dieses Cmdlet exportiert den Inhalt eines Berichts für den DSC-Knoten, der zu der Ressourcengruppe gehört, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ac701-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="ac701-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac701-128">-Confirm</span></span>
<span data-ttu-id="ac701-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac701-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac701-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac701-130">-WhatIf</span></span>
<span data-ttu-id="ac701-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac701-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac701-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac701-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac701-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac701-133">CommonParameters</span></span>
<span data-ttu-id="ac701-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac701-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac701-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac701-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac701-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac701-136">INPUTS</span></span>

### <span data-ttu-id="ac701-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ac701-137">System.Guid</span></span>

### <span data-ttu-id="ac701-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ac701-138">System.String</span></span>

## <span data-ttu-id="ac701-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac701-139">OUTPUTS</span></span>

### <span data-ttu-id="ac701-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="ac701-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="ac701-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ac701-141">NOTES</span></span>

## <span data-ttu-id="ac701-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ac701-142">RELATED LINKS</span></span>

[<span data-ttu-id="ac701-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="ac701-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="ac701-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ac701-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ac701-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="ac701-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


