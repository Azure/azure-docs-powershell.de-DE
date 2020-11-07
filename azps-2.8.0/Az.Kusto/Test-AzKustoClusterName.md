---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650806"
---
# <span data-ttu-id="daf97-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="daf97-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="daf97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="daf97-102">SYNOPSIS</span></span>
<span data-ttu-id="daf97-103">Überprüfen Sie, ob ein angegebener Kusto-Clustername verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="daf97-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="daf97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="daf97-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daf97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf97-105">DESCRIPTION</span></span>
<span data-ttu-id="daf97-106">Überprüfen Sie, ob ein angegebener Kusto-Clustername verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="daf97-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="daf97-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="daf97-107">EXAMPLES</span></span>

### <span data-ttu-id="daf97-108">Beispiel 1: Überprüfen der Verfügbarkeit eines Kusto-Clusternamens, der verwendet wird</span><span class="sxs-lookup"><span data-stu-id="daf97-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="daf97-109">Der obige Befehl gibt zurück, ob ein Kusto-Cluster mit dem Namen "mykustocluster" im Bereich "Central US" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="daf97-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="daf97-110">Beispiel 2: Überprüfen der Verfügbarkeit eines Kusto-Clusternamens, der nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="daf97-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="daf97-111">Der obige Befehl gibt zurück, ob ein Kusto-Cluster mit dem Namen "mykustocluster" im Bereich "Central US" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="daf97-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="daf97-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="daf97-112">PARAMETERS</span></span>

### <span data-ttu-id="daf97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf97-113">-DefaultProfile</span></span>
<span data-ttu-id="daf97-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="daf97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf97-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="daf97-115">-Location</span></span>
<span data-ttu-id="daf97-116">Die Position, an der überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="daf97-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf97-117">-Name</span><span class="sxs-lookup"><span data-stu-id="daf97-117">-Name</span></span>
<span data-ttu-id="daf97-118">Der Name eines bestimmten Clusters.</span><span class="sxs-lookup"><span data-stu-id="daf97-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf97-119">CommonParameters</span></span>
<span data-ttu-id="daf97-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf97-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf97-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf97-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="daf97-122">INPUTS</span></span>

### <span data-ttu-id="daf97-123">Keine</span><span class="sxs-lookup"><span data-stu-id="daf97-123">None</span></span>

## <span data-ttu-id="daf97-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="daf97-124">OUTPUTS</span></span>

### <span data-ttu-id="daf97-125">Microsoft. Azure. Commands. Kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="daf97-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="daf97-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="daf97-126">NOTES</span></span>

## <span data-ttu-id="daf97-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="daf97-127">RELATED LINKS</span></span>
