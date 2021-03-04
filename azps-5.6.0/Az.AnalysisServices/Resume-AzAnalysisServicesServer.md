---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 4a083de76a3b3ebed0f2597f41cc500ddf084f9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945460"
---
# <span data-ttu-id="d6f58-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d6f58-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d6f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f58-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f58-103">Setzt eine Instanz des Analysis Services-Servers fort</span><span class="sxs-lookup"><span data-stu-id="d6f58-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d6f58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6f58-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f58-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6f58-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f58-106">Das Resume-AzAnalysisServicesServer-Cmdlet setzt eine Instanz des Analysis Services-Servers fort.</span><span class="sxs-lookup"><span data-stu-id="d6f58-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d6f58-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6f58-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f58-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6f58-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d6f58-109">Mit diesem Befehl wird ein angehaltener Server mit dem Namen Testserver in der Testgruppe der Ressourcengruppe fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d6f58-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d6f58-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6f58-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f58-111">-DefaultProfile</span></span>
<span data-ttu-id="d6f58-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6f58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f58-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d6f58-113">-Name</span></span>
<span data-ttu-id="d6f58-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="d6f58-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d6f58-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f58-115">-PassThru</span></span>
<span data-ttu-id="d6f58-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d6f58-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d6f58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f58-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6f58-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="d6f58-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f58-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6f58-119">-Confirm</span></span>
<span data-ttu-id="d6f58-120">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="d6f58-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f58-121">-WhatIf</span></span>
<span data-ttu-id="d6f58-122">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen soll, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d6f58-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f58-123">CommonParameters</span></span>
<span data-ttu-id="d6f58-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f58-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f58-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f58-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f58-126">INPUTS</span></span>

### <span data-ttu-id="d6f58-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f58-127">System.String</span></span>

## <span data-ttu-id="d6f58-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6f58-128">OUTPUTS</span></span>

### <span data-ttu-id="d6f58-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d6f58-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d6f58-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6f58-130">NOTES</span></span>
<span data-ttu-id="d6f58-131">Alias: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="d6f58-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="d6f58-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6f58-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6f58-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d6f58-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d6f58-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d6f58-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
