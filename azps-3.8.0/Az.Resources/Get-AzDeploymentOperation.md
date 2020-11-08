---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 9709a21f51b1f0d2b9701257b8c5556698cab228
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996305"
---
# <span data-ttu-id="daa5d-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="daa5d-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="daa5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="daa5d-102">SYNOPSIS</span></span>
<span data-ttu-id="daa5d-103">Abrufen des Bereitstellungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="daa5d-103">Get deployment operation</span></span>

## <span data-ttu-id="daa5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="daa5d-104">SYNTAX</span></span>

### <span data-ttu-id="daa5d-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="daa5d-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daa5d-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="daa5d-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa5d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daa5d-107">DESCRIPTION</span></span>
<span data-ttu-id="daa5d-108">Das Cmdlet " **Get-AzDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="daa5d-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="daa5d-109">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="daa5d-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="daa5d-110">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="daa5d-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="daa5d-111">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="daa5d-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="daa5d-112">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="daa5d-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="daa5d-113">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="daa5d-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="daa5d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="daa5d-114">EXAMPLES</span></span>

### <span data-ttu-id="daa5d-115">Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="daa5d-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="daa5d-116">Ruft den Bereitstellungsvorgang mit dem Namen "Test" im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="daa5d-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="daa5d-117">Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="daa5d-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="daa5d-118">Mit diesem Befehl wird die Bereitstellung "Test" im aktuellen Abonnement Bereich abgerufen und die Bereitstellungsvorgänge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="daa5d-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="daa5d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="daa5d-119">PARAMETERS</span></span>

### <span data-ttu-id="daa5d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="daa5d-120">-ApiVersion</span></span>
<span data-ttu-id="daa5d-121">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="daa5d-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="daa5d-122">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="daa5d-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa5d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa5d-123">-DefaultProfile</span></span>
<span data-ttu-id="daa5d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="daa5d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa5d-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="daa5d-125">-DeploymentName</span></span>
<span data-ttu-id="daa5d-126">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="daa5d-126">The deployment name.</span></span>

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

### <span data-ttu-id="daa5d-127">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="daa5d-127">-DeploymentObject</span></span>
<span data-ttu-id="daa5d-128">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="daa5d-128">The deployment object.</span></span>

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

### <span data-ttu-id="daa5d-129">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="daa5d-129">-OperationId</span></span>
<span data-ttu-id="daa5d-130">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="daa5d-130">The deployment operation Id.</span></span>

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

### <span data-ttu-id="daa5d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="daa5d-131">-Pre</span></span>
<span data-ttu-id="daa5d-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="daa5d-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="daa5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa5d-133">CommonParameters</span></span>
<span data-ttu-id="daa5d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa5d-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daa5d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa5d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="daa5d-136">INPUTS</span></span>

### <span data-ttu-id="daa5d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="daa5d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="daa5d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="daa5d-138">OUTPUTS</span></span>

### <span data-ttu-id="daa5d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="daa5d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="daa5d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="daa5d-140">NOTES</span></span>

## <span data-ttu-id="daa5d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="daa5d-141">RELATED LINKS</span></span>
