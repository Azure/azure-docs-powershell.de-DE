---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159993"
---
# <span data-ttu-id="5b106-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5b106-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="5b106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b106-102">SYNOPSIS</span></span>
<span data-ttu-id="5b106-103">Bereitstellungsvorgang für Bereitstellung im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="5b106-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="5b106-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b106-104">SYNTAX</span></span>

### <span data-ttu-id="5b106-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b106-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b106-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5b106-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b106-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b106-107">DESCRIPTION</span></span>
<span data-ttu-id="5b106-108">Das Cmdlet **"Get-AzTenantDeploymentOperation"** listet alle Vorgänge auf, die Teil der Bereitstellung im aktuellen Mandantenbereich waren, damit Sie die genauen Vorgänge identifizieren und weitere Informationen zu den genauen Vorgängen erhalten können, bei deren Bereitstellung ein Fehler aufteilt war.</span><span class="sxs-lookup"><span data-stu-id="5b106-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="5b106-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b106-109">EXAMPLES</span></span>

### <span data-ttu-id="5b106-110">Beispiel 1: Bereitstellungsvorgänge mit einem Bereitstellungsnamen erhalten</span><span class="sxs-lookup"><span data-stu-id="5b106-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="5b106-111">Ruft Bereitstellungsvorgänge mit dem Namen "Deploy01" im aktuellen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="5b106-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="5b106-112">Beispiel 2: Erhalten einer Bereitstellung und deren Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="5b106-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="5b106-113">Dieser Befehl ruft die Bereitstellung "Deploy01" im aktuellen Mandantenbereich ab und ruft die Bereitstellungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="5b106-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="5b106-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b106-114">PARAMETERS</span></span>

### <span data-ttu-id="5b106-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b106-115">-DefaultProfile</span></span>
<span data-ttu-id="5b106-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b106-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b106-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5b106-117">-DeploymentName</span></span>
<span data-ttu-id="5b106-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="5b106-118">The deployment name.</span></span>

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

### <span data-ttu-id="5b106-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5b106-119">-DeploymentObject</span></span>
<span data-ttu-id="5b106-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b106-120">The deployment object.</span></span>

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

### <span data-ttu-id="5b106-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5b106-121">-OperationId</span></span>
<span data-ttu-id="5b106-122">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="5b106-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="5b106-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b106-123">-Pre</span></span>
<span data-ttu-id="5b106-124">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b106-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5b106-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b106-125">CommonParameters</span></span>
<span data-ttu-id="5b106-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b106-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b106-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b106-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b106-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b106-128">INPUTS</span></span>

### <span data-ttu-id="5b106-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5b106-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5b106-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b106-130">OUTPUTS</span></span>

### <span data-ttu-id="5b106-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5b106-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="5b106-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5b106-132">NOTES</span></span>

## <span data-ttu-id="5b106-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5b106-133">RELATED LINKS</span></span>
