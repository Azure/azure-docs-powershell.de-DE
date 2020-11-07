---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3db7d3b0b27cd49207871ba7b9d47d5b79e661fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843263"
---
# <span data-ttu-id="05713-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="05713-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="05713-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05713-102">SYNOPSIS</span></span>
<span data-ttu-id="05713-103">Entfernt eine Bereitstellung und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="05713-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="05713-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05713-104">SYNTAX</span></span>

### <span data-ttu-id="05713-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="05713-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05713-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="05713-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05713-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="05713-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05713-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05713-108">DESCRIPTION</span></span>
<span data-ttu-id="05713-109">Das Cmdlet **Remove-AzDeployment** entfernt eine Azure-Bereitstellung im Abonnement Bereich und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="05713-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="05713-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05713-110">EXAMPLES</span></span>

### <span data-ttu-id="05713-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="05713-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="05713-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="05713-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="05713-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="05713-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="05713-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="05713-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="05713-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="05713-115">PARAMETERS</span></span>

### <span data-ttu-id="05713-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="05713-116">-ApiVersion</span></span>
<span data-ttu-id="05713-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05713-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="05713-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="05713-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="05713-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05713-119">-AsJob</span></span>
<span data-ttu-id="05713-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="05713-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05713-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05713-121">-DefaultProfile</span></span>
<span data-ttu-id="05713-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05713-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05713-123">-ID</span><span class="sxs-lookup"><span data-stu-id="05713-123">-Id</span></span>
<span data-ttu-id="05713-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="05713-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="05713-125">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="05713-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="05713-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05713-126">-InputObject</span></span>
<span data-ttu-id="05713-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="05713-127">The deployment object.</span></span>

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

### <span data-ttu-id="05713-128">-Name</span><span class="sxs-lookup"><span data-stu-id="05713-128">-Name</span></span>
<span data-ttu-id="05713-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="05713-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="05713-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05713-130">-PassThru</span></span>
<span data-ttu-id="05713-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="05713-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="05713-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="05713-132">-Pre</span></span>
<span data-ttu-id="05713-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="05713-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="05713-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05713-134">-Confirm</span></span>
<span data-ttu-id="05713-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05713-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05713-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05713-136">-WhatIf</span></span>
<span data-ttu-id="05713-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05713-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05713-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05713-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05713-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05713-139">CommonParameters</span></span>
<span data-ttu-id="05713-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05713-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05713-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05713-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05713-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05713-142">INPUTS</span></span>

### <span data-ttu-id="05713-143">System. String</span><span class="sxs-lookup"><span data-stu-id="05713-143">System.String</span></span>

## <span data-ttu-id="05713-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05713-144">OUTPUTS</span></span>

### <span data-ttu-id="05713-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05713-145">System.Boolean</span></span>

## <span data-ttu-id="05713-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="05713-146">NOTES</span></span>

## <span data-ttu-id="05713-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05713-147">RELATED LINKS</span></span>
