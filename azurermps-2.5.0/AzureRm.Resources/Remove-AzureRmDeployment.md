---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 7bd45da18565ae408ec71753f7f4527e53c2e4c1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850568"
---
# <span data-ttu-id="40ffe-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="40ffe-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="40ffe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="40ffe-103">Entfernt eine Bereitstellung und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="40ffe-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ffe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ffe-104">SYNTAX</span></span>

### <span data-ttu-id="40ffe-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="40ffe-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ffe-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="40ffe-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ffe-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="40ffe-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ffe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40ffe-108">DESCRIPTION</span></span>
<span data-ttu-id="40ffe-109">Das Cmdlet **Remove-AzureRmDeployment** entfernt eine Azure-Bereitstellung im Abonnement Bereich und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="40ffe-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="40ffe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40ffe-110">EXAMPLES</span></span>

### <span data-ttu-id="40ffe-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="40ffe-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="40ffe-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="40ffe-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="40ffe-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="40ffe-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="40ffe-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="40ffe-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="40ffe-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="40ffe-115">PARAMETERS</span></span>

### <span data-ttu-id="40ffe-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="40ffe-116">-ApiVersion</span></span>
<span data-ttu-id="40ffe-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40ffe-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="40ffe-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="40ffe-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="40ffe-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40ffe-119">-AsJob</span></span>
<span data-ttu-id="40ffe-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="40ffe-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ffe-121">-DefaultProfile</span></span>
<span data-ttu-id="40ffe-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40ffe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-123">-ID</span><span class="sxs-lookup"><span data-stu-id="40ffe-123">-Id</span></span>
<span data-ttu-id="40ffe-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="40ffe-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="40ffe-125">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="40ffe-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40ffe-126">-InputObject</span></span>
<span data-ttu-id="40ffe-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="40ffe-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-128">-Name</span><span class="sxs-lookup"><span data-stu-id="40ffe-128">-Name</span></span>
<span data-ttu-id="40ffe-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="40ffe-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40ffe-130">-PassThru</span></span>
<span data-ttu-id="40ffe-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="40ffe-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="40ffe-132">-Pre</span></span>
<span data-ttu-id="40ffe-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="40ffe-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40ffe-134">-Confirm</span></span>
<span data-ttu-id="40ffe-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40ffe-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ffe-136">-WhatIf</span></span>
<span data-ttu-id="40ffe-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40ffe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ffe-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40ffe-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ffe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ffe-139">CommonParameters</span></span>
<span data-ttu-id="40ffe-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ffe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ffe-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ffe-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ffe-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40ffe-142">INPUTS</span></span>

### <span data-ttu-id="40ffe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40ffe-143">System.String</span></span>

## <span data-ttu-id="40ffe-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40ffe-144">OUTPUTS</span></span>

### <span data-ttu-id="40ffe-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40ffe-145">System.Boolean</span></span>

## <span data-ttu-id="40ffe-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="40ffe-146">NOTES</span></span>

## <span data-ttu-id="40ffe-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40ffe-147">RELATED LINKS</span></span>
