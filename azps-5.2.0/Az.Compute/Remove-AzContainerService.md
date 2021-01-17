---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291227"
---
# <span data-ttu-id="a065e-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a065e-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="a065e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a065e-102">SYNOPSIS</span></span>
<span data-ttu-id="a065e-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="a065e-103">Removes a container service.</span></span>

## <span data-ttu-id="a065e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a065e-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a065e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a065e-105">DESCRIPTION</span></span>
<span data-ttu-id="a065e-106">Das **Cmdlet "Remove-AzContainerService"** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="a065e-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="a065e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a065e-107">EXAMPLES</span></span>

### <span data-ttu-id="a065e-108">Beispiel 1: Entfernen eines Containerdiensts</span><span class="sxs-lookup"><span data-stu-id="a065e-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a065e-109">Mit diesem Befehl wird der Containerdienst namens CSResourceGroup17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="a065e-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a065e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a065e-110">PARAMETERS</span></span>

### <span data-ttu-id="a065e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a065e-111">-AsJob</span></span>
<span data-ttu-id="a065e-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="a065e-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a065e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a065e-113">-DefaultProfile</span></span>
<span data-ttu-id="a065e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a065e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a065e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a065e-115">-Force</span></span>
<span data-ttu-id="a065e-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a065e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a065e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a065e-117">-Name</span></span>
<span data-ttu-id="a065e-118">Gibt den Namen des Containerdiensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a065e-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a065e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a065e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a065e-120">Gibt die Ressourcengruppe des Containerdiensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a065e-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a065e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a065e-121">-Confirm</span></span>
<span data-ttu-id="a065e-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a065e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a065e-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a065e-123">-WhatIf</span></span>
<span data-ttu-id="a065e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a065e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a065e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a065e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a065e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a065e-126">CommonParameters</span></span>
<span data-ttu-id="a065e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a065e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a065e-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a065e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a065e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a065e-129">INPUTS</span></span>

### <span data-ttu-id="a065e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a065e-130">System.String</span></span>

## <span data-ttu-id="a065e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a065e-131">OUTPUTS</span></span>

### <span data-ttu-id="a065e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a065e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a065e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a065e-133">NOTES</span></span>

## <span data-ttu-id="a065e-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a065e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a065e-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a065e-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="a065e-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a065e-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="a065e-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a065e-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


