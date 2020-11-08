---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176115"
---
# <span data-ttu-id="25c5b-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="25c5b-101">Get-AzDeployment</span></span>

## <span data-ttu-id="25c5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="25c5b-103">Bereitstellung abrufen</span><span class="sxs-lookup"><span data-stu-id="25c5b-103">Get deployment</span></span>

## <span data-ttu-id="25c5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c5b-104">SYNTAX</span></span>

### <span data-ttu-id="25c5b-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="25c5b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25c5b-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="25c5b-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c5b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25c5b-107">DESCRIPTION</span></span>
<span data-ttu-id="25c5b-108">Mit dem Cmdlet **Get-AzDeployment werden** die Bereitstellungen im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="25c5b-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="25c5b-109">Geben Sie den *Namen* oder den *ID-* Parameter an, um die Ergebnisse zu filtern.</span><span class="sxs-lookup"><span data-stu-id="25c5b-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="25c5b-110">Standardmäßig ruft **Get-AzDeployment** alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="25c5b-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="25c5b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25c5b-111">EXAMPLES</span></span>

### <span data-ttu-id="25c5b-112">Beispiel 1: Abrufen aller Bereitstellungen im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="25c5b-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="25c5b-113">Dieser Befehl ruft alle Bereitstellungen im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="25c5b-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="25c5b-114">Beispiel 2: Abrufen einer Bereitstellung nach Name</span><span class="sxs-lookup"><span data-stu-id="25c5b-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="25c5b-115">Mit diesem Befehl wird die DeployRoles01-Bereitstellung im aktuellen Abonnement Bereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="25c5b-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="25c5b-116">Sie können einer Bereitstellung einen Namen zuweisen, wenn Sie Sie mithilfe der Cmdlets **New-AzDeployment** erstellen.</span><span class="sxs-lookup"><span data-stu-id="25c5b-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="25c5b-117">Wenn Sie keinen Namen zuweisen, geben die Cmdlets einen Standardnamen basierend auf der Vorlage an, die zum Erstellen der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25c5b-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="25c5b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="25c5b-118">PARAMETERS</span></span>

### <span data-ttu-id="25c5b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c5b-119">-DefaultProfile</span></span>
<span data-ttu-id="25c5b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25c5b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25c5b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="25c5b-121">-Id</span></span>
<span data-ttu-id="25c5b-122">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="25c5b-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="25c5b-123">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="25c5b-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c5b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="25c5b-124">-Name</span></span>
<span data-ttu-id="25c5b-125">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="25c5b-125">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c5b-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="25c5b-126">-Pre</span></span>
<span data-ttu-id="25c5b-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="25c5b-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="25c5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c5b-128">CommonParameters</span></span>
<span data-ttu-id="25c5b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c5b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25c5b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c5b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25c5b-131">INPUTS</span></span>

### <span data-ttu-id="25c5b-132">Keine</span><span class="sxs-lookup"><span data-stu-id="25c5b-132">None</span></span>

## <span data-ttu-id="25c5b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25c5b-133">OUTPUTS</span></span>

### <span data-ttu-id="25c5b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="25c5b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="25c5b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="25c5b-135">NOTES</span></span>

## <span data-ttu-id="25c5b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25c5b-136">RELATED LINKS</span></span>
