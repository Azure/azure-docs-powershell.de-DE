---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930720"
---
# <span data-ttu-id="0c621-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="0c621-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="0c621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c621-102">SYNOPSIS</span></span>
<span data-ttu-id="0c621-103">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten mit den Azure-Diensten, die von Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0c621-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="0c621-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c621-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="0c621-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c621-105">DESCRIPTION</span></span>
<span data-ttu-id="0c621-106">Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten mit den Azure-Diensten, die von Azure Stack HCI erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0c621-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="0c621-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c621-107">EXAMPLES</span></span>

### <span data-ttu-id="0c621-108">BEISPIEL 1</span><span class="sxs-lookup"><span data-stu-id="0c621-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="0c621-109">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="0c621-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="0c621-110">Erfolgsfall.</span><span class="sxs-lookup"><span data-stu-id="0c621-110">Success case.</span></span>

### <span data-ttu-id="0c621-111">BEISPIEL 2</span><span class="sxs-lookup"><span data-stu-id="0c621-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="0c621-112">Aufrufen eines Clusterknotens</span><span class="sxs-lookup"><span data-stu-id="0c621-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="0c621-113">Fehlgeschlagener Fall.</span><span class="sxs-lookup"><span data-stu-id="0c621-113">Failed case.</span></span>

## <span data-ttu-id="0c621-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c621-114">PARAMETERS</span></span>

### <span data-ttu-id="0c621-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="0c621-115">-ComputerName</span></span>
<span data-ttu-id="0c621-116">Gibt einen der Clusterknoten im lokalen Cluster an, der bei Azure registriert wird.</span><span class="sxs-lookup"><span data-stu-id="0c621-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="0c621-117">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="0c621-117">-Credential</span></span>
<span data-ttu-id="0c621-118">Gibt die Anmeldeinformationen für den Computernamen an.</span><span class="sxs-lookup"><span data-stu-id="0c621-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="0c621-119">Standardmäßig wird das Cmdlet vom aktuellen Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c621-119">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="0c621-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0c621-120">-EnvironmentName</span></span>
<span data-ttu-id="0c621-121">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="0c621-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="0c621-122">Standardmäßig ist AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="0c621-122">Default is AzureCloud.</span></span>
<span data-ttu-id="0c621-123">Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="0c621-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="0c621-124">-Region</span><span class="sxs-lookup"><span data-stu-id="0c621-124">-Region</span></span>
<span data-ttu-id="0c621-125">Gibt die Region an, mit der eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c621-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="0c621-126">Wird nur verwendet, wenn es sich um eine Kanarenregion handelt.</span><span class="sxs-lookup"><span data-stu-id="0c621-126">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="0c621-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c621-127">CommonParameters</span></span>
<span data-ttu-id="0c621-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c621-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c621-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c621-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c621-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c621-130">INPUTS</span></span>

## <span data-ttu-id="0c621-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c621-131">OUTPUTS</span></span>

### <span data-ttu-id="0c621-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="0c621-132">PSCustomObject.</span></span> <span data-ttu-id="0c621-133">Gibt folgende Eigenschaften in PSCustomObject zurück.</span><span class="sxs-lookup"><span data-stu-id="0c621-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="0c621-134">Test: Name des durchgeführten Tests.</span><span class="sxs-lookup"><span data-stu-id="0c621-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="0c621-135">EndpunktTested: Endpunkt, der im Test verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c621-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="0c621-136">IsRequired: True or False</span><span class="sxs-lookup"><span data-stu-id="0c621-136">IsRequired: True or False</span></span>
### <span data-ttu-id="0c621-137">Ergebnis: Erfolgreich oder fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="0c621-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="0c621-138">FailedNodes: Liste der Knoten, bei denen der Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0c621-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="0c621-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c621-139">NOTES</span></span>

## <span data-ttu-id="0c621-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c621-140">RELATED LINKS</span></span>
