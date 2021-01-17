---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460395"
---
# <span data-ttu-id="bb615-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="bb615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb615-102">SYNOPSIS</span></span>
<span data-ttu-id="bb615-103">Entfernt einen Azure-App-Dienstplan.</span><span class="sxs-lookup"><span data-stu-id="bb615-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="bb615-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb615-104">SYNTAX</span></span>

### <span data-ttu-id="bb615-105">S1</span><span class="sxs-lookup"><span data-stu-id="bb615-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb615-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb615-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb615-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb615-107">DESCRIPTION</span></span>
<span data-ttu-id="bb615-108">Das **Cmdlet "Remove-AzAppServicePlan"** entfernt einen Azure App Service-Plan.</span><span class="sxs-lookup"><span data-stu-id="bb615-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="bb615-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb615-109">EXAMPLES</span></span>

### <span data-ttu-id="bb615-110">Beispiel 1: Entfernen eines App -Dienstplans</span><span class="sxs-lookup"><span data-stu-id="bb615-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="bb615-111">Mit diesem Befehl wird der Azure-App-Dienstplan "ContosoASP" entfernt, der zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="bb615-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bb615-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb615-112">PARAMETERS</span></span>

### <span data-ttu-id="bb615-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-113">-AppServicePlan</span></span>
<span data-ttu-id="bb615-114">App Service Plan Object</span><span class="sxs-lookup"><span data-stu-id="bb615-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb615-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb615-115">-AsJob</span></span>
<span data-ttu-id="bb615-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bb615-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb615-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb615-117">-DefaultProfile</span></span>
<span data-ttu-id="bb615-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb615-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb615-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bb615-119">-Force</span></span>
<span data-ttu-id="bb615-120">Option "Erzwingend entfernen"</span><span class="sxs-lookup"><span data-stu-id="bb615-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="bb615-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bb615-121">-Name</span></span>
<span data-ttu-id="bb615-122">Name des App-Serviceplans</span><span class="sxs-lookup"><span data-stu-id="bb615-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb615-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb615-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb615-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bb615-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb615-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb615-125">-Confirm</span></span>
<span data-ttu-id="bb615-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb615-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb615-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb615-127">-WhatIf</span></span>
<span data-ttu-id="bb615-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb615-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb615-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb615-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb615-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb615-130">CommonParameters</span></span>
<span data-ttu-id="bb615-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb615-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb615-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb615-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb615-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb615-133">INPUTS</span></span>

### <span data-ttu-id="bb615-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="bb615-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb615-135">OUTPUTS</span></span>

### <span data-ttu-id="bb615-136">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb615-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bb615-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb615-137">NOTES</span></span>

## <span data-ttu-id="bb615-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb615-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb615-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="bb615-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="bb615-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb615-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


