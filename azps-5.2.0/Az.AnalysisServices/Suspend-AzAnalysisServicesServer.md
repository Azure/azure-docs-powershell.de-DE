---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303675"
---
# <span data-ttu-id="c12c7-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c12c7-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c12c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c12c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c12c7-103">Eine Instanz des Analysis Services -Servers wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="c12c7-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="c12c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c12c7-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c12c7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c12c7-105">DESCRIPTION</span></span>
<span data-ttu-id="c12c7-106">Das Suspend-AzAnalysisServicesServer cmdlet suspends a instance of Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="c12c7-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="c12c7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c12c7-107">EXAMPLES</span></span>

### <span data-ttu-id="c12c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c12c7-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c12c7-109">Mit diesem Befehl wird ein aktiver Server namens "Testserver" in der Testgruppe der Ressourcengruppe angehalten.</span><span class="sxs-lookup"><span data-stu-id="c12c7-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c12c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c12c7-110">PARAMETERS</span></span>

### <span data-ttu-id="c12c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12c7-111">-DefaultProfile</span></span>
<span data-ttu-id="c12c7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c12c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c12c7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c12c7-113">-Name</span></span>
<span data-ttu-id="c12c7-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="c12c7-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c12c7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c12c7-115">-PassThru</span></span>
<span data-ttu-id="c12c7-116">Gibt die gelöschten Serverdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c12c7-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="c12c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c12c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c12c7-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="c12c7-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="c12c7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c12c7-119">-Confirm</span></span>
<span data-ttu-id="c12c7-120">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="c12c7-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="c12c7-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c12c7-121">-WhatIf</span></span>
<span data-ttu-id="c12c7-122">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen wird, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c12c7-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="c12c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12c7-123">CommonParameters</span></span>
<span data-ttu-id="c12c7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12c7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c12c7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12c7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c12c7-126">INPUTS</span></span>

### <span data-ttu-id="c12c7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c12c7-127">System.String</span></span>

## <span data-ttu-id="c12c7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c12c7-128">OUTPUTS</span></span>

### <span data-ttu-id="c12c7-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c12c7-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="c12c7-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c12c7-130">NOTES</span></span>
<span data-ttu-id="c12c7-131">Alias: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="c12c7-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="c12c7-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c12c7-132">RELATED LINKS</span></span>

[<span data-ttu-id="c12c7-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c12c7-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c12c7-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c12c7-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

