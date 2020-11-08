---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176086"
---
# <span data-ttu-id="a3d6f-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3d6f-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="a3d6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d6f-103">Entfernt eine Bereitstellung und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a3d6f-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="a3d6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d6f-104">SYNTAX</span></span>

### <span data-ttu-id="a3d6f-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3d6f-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d6f-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a3d6f-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d6f-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3d6f-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d6f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="a3d6f-109">Das Cmdlet **Remove-AzDeployment** entfernt eine Azure-Bereitstellung im Abonnement Bereich und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="a3d6f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="a3d6f-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="a3d6f-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="a3d6f-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="a3d6f-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="a3d6f-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="a3d6f-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="a3d6f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d6f-115">PARAMETERS</span></span>

### <span data-ttu-id="a3d6f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3d6f-116">-AsJob</span></span>
<span data-ttu-id="a3d6f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3d6f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3d6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d6f-118">-DefaultProfile</span></span>
<span data-ttu-id="a3d6f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d6f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="a3d6f-120">-Id</span></span>
<span data-ttu-id="a3d6f-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a3d6f-122">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a3d6f-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d6f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3d6f-123">-InputObject</span></span>
<span data-ttu-id="a3d6f-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d6f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a3d6f-125">-Name</span></span>
<span data-ttu-id="a3d6f-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d6f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d6f-127">-PassThru</span></span>
<span data-ttu-id="a3d6f-128">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a3d6f-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a3d6f-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="a3d6f-129">-Pre</span></span>
<span data-ttu-id="a3d6f-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a3d6f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3d6f-131">-Confirm</span></span>
<span data-ttu-id="a3d6f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d6f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d6f-133">-WhatIf</span></span>
<span data-ttu-id="a3d6f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d6f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d6f-136">CommonParameters</span></span>
<span data-ttu-id="a3d6f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d6f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3d6f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d6f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3d6f-139">INPUTS</span></span>

### <span data-ttu-id="a3d6f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a3d6f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a3d6f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3d6f-141">OUTPUTS</span></span>

### <span data-ttu-id="a3d6f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d6f-142">System.Boolean</span></span>

## <span data-ttu-id="a3d6f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3d6f-143">NOTES</span></span>

## <span data-ttu-id="a3d6f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3d6f-144">RELATED LINKS</span></span>
