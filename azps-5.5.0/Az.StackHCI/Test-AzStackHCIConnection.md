---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145497"
---
# <span data-ttu-id="fdd0f-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="fdd0f-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="fdd0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdd0f-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd0f-103">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="fdd0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdd0f-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="fdd0f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd0f-105">DESCRIPTION</span></span>
<span data-ttu-id="fdd0f-106">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="fdd0f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdd0f-107">EXAMPLES</span></span>

### <span data-ttu-id="fdd0f-108">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="fdd0f-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="fdd0f-109">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="fdd0f-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="fdd0f-110">Erfolgsfall.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-110">Success case.</span></span>

### <span data-ttu-id="fdd0f-111">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="fdd0f-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="fdd0f-112">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="fdd0f-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="fdd0f-113">Fehler im Fall eines Fehlers.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-113">Failed case.</span></span>

## <span data-ttu-id="fdd0f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdd0f-114">PARAMETERS</span></span>

### <span data-ttu-id="fdd0f-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="fdd0f-115">-ComputerName</span></span>
<span data-ttu-id="fdd0f-116">Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd0f-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="fdd0f-117">-Credential</span></span>
<span data-ttu-id="fdd0f-118">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="fdd0f-119">Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-119">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd0f-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="fdd0f-120">-EnvironmentName</span></span>
<span data-ttu-id="fdd0f-121">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="fdd0f-122">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-122">Default is AzureCloud.</span></span>
<span data-ttu-id="fdd0f-123">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="fdd0f-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd0f-124">-Region</span><span class="sxs-lookup"><span data-stu-id="fdd0f-124">-Region</span></span>
<span data-ttu-id="fdd0f-125">Gibt die Region an, mit der eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="fdd0f-126">Wird nur verwendet, wenn es sich um eine Canary-Region handelt.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-126">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd0f-127">CommonParameters</span></span>
<span data-ttu-id="fdd0f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd0f-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdd0f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd0f-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdd0f-130">INPUTS</span></span>

## <span data-ttu-id="fdd0f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdd0f-131">OUTPUTS</span></span>

### <span data-ttu-id="fdd0f-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-132">PSCustomObject.</span></span> <span data-ttu-id="fdd0f-133">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="fdd0f-134">Test: Name des ausgeführten Tests.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="fdd0f-135">EndpointTested: Im Test verwendeter Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="fdd0f-136">IsRequired: True or False</span><span class="sxs-lookup"><span data-stu-id="fdd0f-136">IsRequired: True or False</span></span>
### <span data-ttu-id="fdd0f-137">Ergebnis: Erfolgreich oder fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="fdd0f-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="fdd0f-138">FailedNodes: Liste der Knoten, bei denen der Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fdd0f-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="fdd0f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fdd0f-139">NOTES</span></span>

## <span data-ttu-id="fdd0f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fdd0f-140">RELATED LINKS</span></span>
