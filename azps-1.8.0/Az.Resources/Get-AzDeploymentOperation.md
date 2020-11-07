---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 809e7e82948d155ad73a80cbd430499d5372b644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659652"
---
# <span data-ttu-id="c8faa-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c8faa-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="c8faa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8faa-102">SYNOPSIS</span></span>
<span data-ttu-id="c8faa-103">Abrufen des Bereitstellungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="c8faa-103">Get deployment operation</span></span>

## <span data-ttu-id="c8faa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8faa-104">SYNTAX</span></span>

### <span data-ttu-id="c8faa-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8faa-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8faa-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c8faa-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8faa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8faa-107">DESCRIPTION</span></span>
<span data-ttu-id="c8faa-108">Das Cmdlet " **Get-AzDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="c8faa-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c8faa-109">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c8faa-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="c8faa-110">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8faa-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="c8faa-111">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="c8faa-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="c8faa-112">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c8faa-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="c8faa-113">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="c8faa-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="c8faa-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8faa-114">EXAMPLES</span></span>

### <span data-ttu-id="c8faa-115">Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="c8faa-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="c8faa-116">Ruft den Bereitstellungsvorgang mit dem Namen "Test" im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c8faa-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="c8faa-117">Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="c8faa-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="c8faa-118">Mit diesem Befehl wird die Bereitstellung "Test" im aktuellen Abonnement Bereich abgerufen und die Bereitstellungsvorgänge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8faa-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="c8faa-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8faa-119">PARAMETERS</span></span>

### <span data-ttu-id="c8faa-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c8faa-120">-ApiVersion</span></span>
<span data-ttu-id="c8faa-121">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8faa-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c8faa-122">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c8faa-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c8faa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8faa-123">-DefaultProfile</span></span>
<span data-ttu-id="c8faa-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8faa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8faa-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c8faa-125">-DeploymentName</span></span>
<span data-ttu-id="c8faa-126">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="c8faa-126">The deployment name.</span></span>

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

### <span data-ttu-id="c8faa-127">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="c8faa-127">-DeploymentObject</span></span>
<span data-ttu-id="c8faa-128">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c8faa-128">The deployment object.</span></span>

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

### <span data-ttu-id="c8faa-129">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="c8faa-129">-OperationId</span></span>
<span data-ttu-id="c8faa-130">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="c8faa-130">The deployment operation Id.</span></span>

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

### <span data-ttu-id="c8faa-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c8faa-131">-Pre</span></span>
<span data-ttu-id="c8faa-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c8faa-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c8faa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8faa-133">CommonParameters</span></span>
<span data-ttu-id="c8faa-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8faa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8faa-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8faa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8faa-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8faa-136">INPUTS</span></span>

### <span data-ttu-id="c8faa-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c8faa-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c8faa-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8faa-138">OUTPUTS</span></span>

### <span data-ttu-id="c8faa-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c8faa-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c8faa-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8faa-140">NOTES</span></span>

## <span data-ttu-id="c8faa-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8faa-141">RELATED LINKS</span></span>
