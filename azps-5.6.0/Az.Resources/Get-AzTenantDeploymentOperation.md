---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: cf48e14ded4dd227cb241a341339861bae3a269a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942131"
---
# <span data-ttu-id="99acf-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="99acf-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="99acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99acf-102">SYNOPSIS</span></span>
<span data-ttu-id="99acf-103">Bereitstellungsvorgang für die Bereitstellung im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="99acf-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="99acf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99acf-104">SYNTAX</span></span>

### <span data-ttu-id="99acf-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="99acf-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99acf-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="99acf-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99acf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99acf-107">DESCRIPTION</span></span>
<span data-ttu-id="99acf-108">Das **Cmdlet Get-AzTenantDeploymentOperation** listet alle Vorgänge auf, die Teil der Bereitstellung im aktuellen Mandantenbereich waren, um Ihnen zu helfen, die genauen Vorgänge zu identifizieren und zu geben, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="99acf-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="99acf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99acf-109">EXAMPLES</span></span>

### <span data-ttu-id="99acf-110">Beispiel 1: Erhalten von Bereitstellungsvorgängen mit einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="99acf-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="99acf-111">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" im aktuellen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="99acf-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="99acf-112">Beispiel 2: Erhalten einer Bereitstellung und Deren Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="99acf-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="99acf-113">Dieser Befehl ruft die Bereitstellung "Deploy01" im aktuellen Mandantenbereich ab und ruft die Bereitstellungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="99acf-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="99acf-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99acf-114">PARAMETERS</span></span>

### <span data-ttu-id="99acf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99acf-115">-DefaultProfile</span></span>
<span data-ttu-id="99acf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99acf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99acf-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="99acf-117">-DeploymentName</span></span>
<span data-ttu-id="99acf-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="99acf-118">The deployment name.</span></span>

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

### <span data-ttu-id="99acf-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="99acf-119">-DeploymentObject</span></span>
<span data-ttu-id="99acf-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="99acf-120">The deployment object.</span></span>

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

### <span data-ttu-id="99acf-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="99acf-121">-OperationId</span></span>
<span data-ttu-id="99acf-122">Die Id des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="99acf-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="99acf-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="99acf-123">-Pre</span></span>
<span data-ttu-id="99acf-124">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99acf-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="99acf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99acf-125">CommonParameters</span></span>
<span data-ttu-id="99acf-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99acf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99acf-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99acf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99acf-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99acf-128">INPUTS</span></span>

### <span data-ttu-id="99acf-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="99acf-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="99acf-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99acf-130">OUTPUTS</span></span>

### <span data-ttu-id="99acf-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="99acf-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="99acf-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99acf-132">NOTES</span></span>

## <span data-ttu-id="99acf-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99acf-133">RELATED LINKS</span></span>
