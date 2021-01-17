---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459488"
---
# <span data-ttu-id="eb684-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="eb684-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="eb684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb684-102">SYNOPSIS</span></span>
<span data-ttu-id="eb684-103">Bereitstellungsvorgang</span><span class="sxs-lookup"><span data-stu-id="eb684-103">Get deployment operation</span></span>

## <span data-ttu-id="eb684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb684-104">SYNTAX</span></span>

### <span data-ttu-id="eb684-105">GetByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb684-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb684-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="eb684-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb684-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb684-107">DESCRIPTION</span></span>
<span data-ttu-id="eb684-108">Das **Cmdlet "Get-AzDeploymentOperation"** listet alle Vorgänge auf, die Teil einer Bereitstellung waren, um Sie bei der Identifizierung und Bereitstellung genauerer Informationen zu den genauen Vorgängen zu unterstützen, die bei einer bestimmten Bereitstellung fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="eb684-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="eb684-109">Sie kann auch die Antwort und den Anforderungsinhalt für jeden Bereitstellungsvorgang anzeigen.</span><span class="sxs-lookup"><span data-stu-id="eb684-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="eb684-110">Dies sind die gleichen Informationen, die in den Bereitstellungsdetails auf dem Portal bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="eb684-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="eb684-111">Um die Anforderung und den Antwortinhalt zu erhalten, aktivieren Sie die Einstellung beim Übermitteln einer Bereitstellung über **"New-AzDeployment".**</span><span class="sxs-lookup"><span data-stu-id="eb684-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="eb684-112">Es kann potenziell geheime Daten protokollieren und verfügbar machen, z. B. Kennwörter, die in den Ressourceneigenschafts- oder listKeys-Vorgängen verwendet werden, die beim Abrufen der **Bereitstellungsvorgänge** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eb684-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="eb684-113">Weitere Informationen zu dieser Einstellung und deren Aktivierung finden Sie unter New-AzDeployment und Debuggen ARM Vorlagenbereitstellungen.</span><span class="sxs-lookup"><span data-stu-id="eb684-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="eb684-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb684-114">EXAMPLES</span></span>

### <span data-ttu-id="eb684-115">Beispiel 1: Bereitstellungsvorgänge mit einem Bereitstellungsnamen erhalten</span><span class="sxs-lookup"><span data-stu-id="eb684-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="eb684-116">Ruft den Bereitstellungsvorgang mit dem Namen "test" im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="eb684-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="eb684-117">Beispiel 2: Erhalten einer Bereitstellung und deren Bereitstellungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="eb684-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="eb684-118">Dieser Befehl ruft den Bereitstellungstest im aktuellen Abonnementbereich ab und ruft dessen Bereitstellungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="eb684-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="eb684-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb684-119">PARAMETERS</span></span>

### <span data-ttu-id="eb684-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb684-120">-DefaultProfile</span></span>
<span data-ttu-id="eb684-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb684-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb684-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="eb684-122">-DeploymentName</span></span>
<span data-ttu-id="eb684-123">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="eb684-123">The deployment name.</span></span>

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

### <span data-ttu-id="eb684-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="eb684-124">-DeploymentObject</span></span>
<span data-ttu-id="eb684-125">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="eb684-125">The deployment object.</span></span>

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

### <span data-ttu-id="eb684-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="eb684-126">-OperationId</span></span>
<span data-ttu-id="eb684-127">Die ID des Bereitstellungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="eb684-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="eb684-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb684-128">-Pre</span></span>
<span data-ttu-id="eb684-129">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb684-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eb684-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb684-130">CommonParameters</span></span>
<span data-ttu-id="eb684-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb684-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb684-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb684-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb684-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb684-133">INPUTS</span></span>

### <span data-ttu-id="eb684-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="eb684-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="eb684-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb684-135">OUTPUTS</span></span>

### <span data-ttu-id="eb684-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEploymentOperation</span><span class="sxs-lookup"><span data-stu-id="eb684-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="eb684-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb684-137">NOTES</span></span>

## <span data-ttu-id="eb684-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb684-138">RELATED LINKS</span></span>
