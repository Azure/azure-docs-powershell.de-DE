---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301060"
---
# <span data-ttu-id="da001-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="da001-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="da001-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da001-102">SYNOPSIS</span></span>
<span data-ttu-id="da001-103">Abrufen des Bereitstellungsvorgangs für die Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="da001-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="da001-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da001-104">SYNTAX</span></span>

### <span data-ttu-id="da001-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="da001-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da001-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="da001-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da001-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da001-107">DESCRIPTION</span></span>
<span data-ttu-id="da001-108">Das Cmdlet " **Get-AzTenantDeploymentOperation** " listet alle Vorgänge auf, die Teil der Bereitstellung im aktuellen MANDANTENBEREICH waren, um Ihnen zu helfen, weitere Informationen zu den genauen Vorgängen zu finden, die für eine bestimmte Bereitstellung fehlschlugen.</span><span class="sxs-lookup"><span data-stu-id="da001-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="da001-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da001-109">EXAMPLES</span></span>

### <span data-ttu-id="da001-110">Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="da001-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="da001-111">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" im aktuellen MANDANTENBEREICH ab.</span><span class="sxs-lookup"><span data-stu-id="da001-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="da001-112">Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="da001-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="da001-113">Dieser Befehl ruft die Bereitstellung "Deploy01" im aktuellen MANDANTENBEREICH ab und erhält dessen Bereitstellungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="da001-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="da001-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="da001-114">PARAMETERS</span></span>

### <span data-ttu-id="da001-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da001-115">-DefaultProfile</span></span>
<span data-ttu-id="da001-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da001-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da001-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="da001-117">-DeploymentName</span></span>
<span data-ttu-id="da001-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="da001-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da001-119">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="da001-119">-DeploymentObject</span></span>
<span data-ttu-id="da001-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="da001-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da001-121">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="da001-121">-OperationId</span></span>
<span data-ttu-id="da001-122">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="da001-122">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da001-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="da001-123">-Pre</span></span>
<span data-ttu-id="da001-124">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="da001-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="da001-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da001-125">CommonParameters</span></span>
<span data-ttu-id="da001-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da001-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da001-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da001-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da001-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da001-128">INPUTS</span></span>

### <span data-ttu-id="da001-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="da001-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="da001-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da001-130">OUTPUTS</span></span>

### <span data-ttu-id="da001-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="da001-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="da001-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="da001-132">NOTES</span></span>

## <span data-ttu-id="da001-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da001-133">RELATED LINKS</span></span>
