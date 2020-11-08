---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176113"
---
# <span data-ttu-id="d6032-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d6032-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="d6032-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6032-102">SYNOPSIS</span></span>
<span data-ttu-id="d6032-103">Abrufen des Bereitstellungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="d6032-103">Get deployment operation</span></span>

## <span data-ttu-id="d6032-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6032-104">SYNTAX</span></span>

### <span data-ttu-id="d6032-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6032-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6032-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d6032-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6032-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6032-107">DESCRIPTION</span></span>
<span data-ttu-id="d6032-108">Das Cmdlet " **Get-AzDeploymentOperation** " listet alle Vorgänge auf, die Teil einer Bereitstellung waren, damit Sie weitere Informationen zu den exakten Vorgängen finden können, die für eine bestimmte Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="d6032-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d6032-109">Außerdem kann die Antwort und der Anforderungs Inhalt für jeden Bereitstellungsvorgang angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6032-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="d6032-110">Hierbei handelt es sich um dieselben Informationen, die in den Bereitstellungsdetails im Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6032-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="d6032-111">Um die Anforderung und den Antwortinhalt abzurufen, aktivieren Sie diese Einstellung, wenn Sie eine Bereitstellung über **New-AzDeployment** übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d6032-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="d6032-112">Sie kann potenziell Geheimnisse wie Kennwörter protokollieren und verfügbar machen, die in den Ressourceneigenschaften-oder **listKeys** -Vorgängen verwendet werden, die beim Abrufen der Bereitstellungsvorgänge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6032-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="d6032-113">Weitere Informationen zu dieser Einstellung und dazu, wie Sie Sie aktivieren, finden Sie unter New-AzDeployment und Debuggen von Arm-Vorlagen Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="d6032-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="d6032-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6032-114">EXAMPLES</span></span>

### <span data-ttu-id="d6032-115">Beispiel 1: Abrufen von Bereitstellungsvorgängen bei einem Bereitstellungsnamen</span><span class="sxs-lookup"><span data-stu-id="d6032-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="d6032-116">Ruft den Bereitstellungsvorgang mit dem Namen "Test" im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="d6032-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="d6032-117">Beispiel 2: Abrufen einer Bereitstellung und Abrufen der Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="d6032-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="d6032-118">Mit diesem Befehl wird die Bereitstellung "Test" im aktuellen Abonnement Bereich abgerufen und die Bereitstellungsvorgänge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6032-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="d6032-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6032-119">PARAMETERS</span></span>

### <span data-ttu-id="d6032-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6032-120">-DefaultProfile</span></span>
<span data-ttu-id="d6032-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6032-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6032-122">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="d6032-122">-DeploymentName</span></span>
<span data-ttu-id="d6032-123">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="d6032-123">The deployment name.</span></span>

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

### <span data-ttu-id="d6032-124">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="d6032-124">-DeploymentObject</span></span>
<span data-ttu-id="d6032-125">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d6032-125">The deployment object.</span></span>

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

### <span data-ttu-id="d6032-126">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="d6032-126">-OperationId</span></span>
<span data-ttu-id="d6032-127">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="d6032-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="d6032-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6032-128">-Pre</span></span>
<span data-ttu-id="d6032-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d6032-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6032-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6032-130">CommonParameters</span></span>
<span data-ttu-id="d6032-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6032-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6032-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6032-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6032-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6032-133">INPUTS</span></span>

### <span data-ttu-id="d6032-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d6032-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d6032-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6032-135">OUTPUTS</span></span>

### <span data-ttu-id="d6032-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d6032-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d6032-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6032-137">NOTES</span></span>

## <span data-ttu-id="d6032-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6032-138">RELATED LINKS</span></span>
