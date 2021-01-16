---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374253"
---
# <span data-ttu-id="fff41-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="fff41-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="fff41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff41-102">SYNOPSIS</span></span>
<span data-ttu-id="fff41-103">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fff41-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="fff41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fff41-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="fff41-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff41-105">DESCRIPTION</span></span>
<span data-ttu-id="fff41-106">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fff41-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="fff41-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fff41-107">EXAMPLES</span></span>

### <span data-ttu-id="fff41-108">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="fff41-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="fff41-109">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span><span class="sxs-lookup"><span data-stu-id="fff41-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="fff41-110">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="fff41-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="fff41-111">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="fff41-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="fff41-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff41-112">PARAMETERS</span></span>

### <span data-ttu-id="fff41-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="fff41-113">-ComputerName</span></span>
<span data-ttu-id="fff41-114">Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="fff41-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="fff41-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="fff41-115">-Credential</span></span>
<span data-ttu-id="fff41-116">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="fff41-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="fff41-117">Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fff41-117">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="fff41-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="fff41-118">-EnvironmentName</span></span>
<span data-ttu-id="fff41-119">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="fff41-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="fff41-120">Der Standardwert ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="fff41-120">Default is AzureCloud.</span></span>
<span data-ttu-id="fff41-121">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="fff41-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="fff41-122">-Region</span><span class="sxs-lookup"><span data-stu-id="fff41-122">-Region</span></span>
<span data-ttu-id="fff41-123">Gibt die Region an, mit der eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fff41-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="fff41-124">Wird nur verwendet, wenn es sich um eine Canary-Region handelt.</span><span class="sxs-lookup"><span data-stu-id="fff41-124">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="fff41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff41-125">CommonParameters</span></span>
<span data-ttu-id="fff41-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff41-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff41-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff41-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fff41-128">INPUTS</span></span>

## <span data-ttu-id="fff41-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fff41-129">OUTPUTS</span></span>

### <span data-ttu-id="fff41-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="fff41-130">PSCustomObject.</span></span> <span data-ttu-id="fff41-131">Gibt die folgenden Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="fff41-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="fff41-132">Test: Name des ausgeführten Tests.</span><span class="sxs-lookup"><span data-stu-id="fff41-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="fff41-133">EndpointTested: Der im Test verwendete Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="fff41-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="fff41-134">IsRequired: True or False</span><span class="sxs-lookup"><span data-stu-id="fff41-134">IsRequired: True or False</span></span>
### <span data-ttu-id="fff41-135">Ergebnis: Erfolgreich oder fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="fff41-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="fff41-136">FailedNodes: Liste der Knoten, bei denen der Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fff41-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="fff41-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fff41-137">NOTES</span></span>

## <span data-ttu-id="fff41-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fff41-138">RELATED LINKS</span></span>
