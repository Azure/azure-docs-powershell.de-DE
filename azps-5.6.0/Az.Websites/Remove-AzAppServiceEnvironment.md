---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927656"
---
# <span data-ttu-id="a71df-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a71df-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="a71df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a71df-102">SYNOPSIS</span></span>
<span data-ttu-id="a71df-103">Entfernen Sie die App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="a71df-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="a71df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a71df-104">SYNTAX</span></span>

### <span data-ttu-id="a71df-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="a71df-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a71df-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a71df-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71df-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a71df-107">DESCRIPTION</span></span>
<span data-ttu-id="a71df-108">Das **Cmdlet Remove-AzAppServiceEnvironment** entfernt eine App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="a71df-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="a71df-109">Jeder App-Dienstplan muss vor dem Löschen des ASE gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a71df-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="a71df-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a71df-110">EXAMPLES</span></span>

### <span data-ttu-id="a71df-111">Beispiel 1: Löschen einer App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="a71df-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="a71df-112">Löschen einer App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="a71df-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="a71df-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a71df-113">PARAMETERS</span></span>

### <span data-ttu-id="a71df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a71df-114">-AsJob</span></span>
<span data-ttu-id="a71df-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="a71df-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a71df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71df-116">-DefaultProfile</span></span>
<span data-ttu-id="a71df-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a71df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a71df-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a71df-118">-Force</span></span>
<span data-ttu-id="a71df-119">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="a71df-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a71df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a71df-120">-InputObject</span></span>
<span data-ttu-id="a71df-121">Das App-Dienstumgebungsobjekt</span><span class="sxs-lookup"><span data-stu-id="a71df-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a71df-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a71df-122">-Name</span></span>
<span data-ttu-id="a71df-123">Der Name der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="a71df-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a71df-124">-PassThru</span></span>
<span data-ttu-id="a71df-125">Rückgabestatus.</span><span class="sxs-lookup"><span data-stu-id="a71df-125">Return status.</span></span>

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

### <span data-ttu-id="a71df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a71df-126">-ResourceGroupName</span></span>
<span data-ttu-id="a71df-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a71df-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71df-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a71df-128">-Confirm</span></span>
<span data-ttu-id="a71df-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a71df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71df-130">-WhatIf</span></span>
<span data-ttu-id="a71df-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a71df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a71df-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a71df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71df-133">CommonParameters</span></span>
<span data-ttu-id="a71df-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71df-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a71df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71df-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a71df-136">INPUTS</span></span>

### <span data-ttu-id="a71df-137">Keine</span><span class="sxs-lookup"><span data-stu-id="a71df-137">None</span></span>

## <span data-ttu-id="a71df-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a71df-138">OUTPUTS</span></span>

### <span data-ttu-id="a71df-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="a71df-139">System.Object</span></span>
## <span data-ttu-id="a71df-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a71df-140">NOTES</span></span>

## <span data-ttu-id="a71df-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a71df-141">RELATED LINKS</span></span>

[<span data-ttu-id="a71df-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a71df-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="a71df-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a71df-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="a71df-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="a71df-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)