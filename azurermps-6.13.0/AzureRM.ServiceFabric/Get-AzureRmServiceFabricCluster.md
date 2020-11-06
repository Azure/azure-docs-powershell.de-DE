---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501061"
---
# <span data-ttu-id="07462-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="07462-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="07462-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07462-102">SYNOPSIS</span></span>
<span data-ttu-id="07462-103">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="07462-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07462-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07462-104">SYNTAX</span></span>

### <span data-ttu-id="07462-105">BySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="07462-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07462-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07462-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07462-107">ByName</span><span class="sxs-lookup"><span data-stu-id="07462-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07462-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07462-108">DESCRIPTION</span></span>
<span data-ttu-id="07462-109">Der **Get-AzureRmServiceFabricCluster** erhält die Clusterressourcen Details.</span><span class="sxs-lookup"><span data-stu-id="07462-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="07462-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07462-110">EXAMPLES</span></span>

### <span data-ttu-id="07462-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07462-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="07462-112">Dieser Befehl erhält die Clusterressourcen Details für Cluster "mycluster".</span><span class="sxs-lookup"><span data-stu-id="07462-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="07462-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="07462-113">PARAMETERS</span></span>

### <span data-ttu-id="07462-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07462-114">-DefaultProfile</span></span>
<span data-ttu-id="07462-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07462-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07462-116">-Name</span><span class="sxs-lookup"><span data-stu-id="07462-116">-Name</span></span>
<span data-ttu-id="07462-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="07462-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07462-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07462-118">-ResourceGroupName</span></span>
<span data-ttu-id="07462-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07462-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07462-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07462-120">CommonParameters</span></span>
<span data-ttu-id="07462-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07462-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07462-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07462-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07462-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07462-123">INPUTS</span></span>

### <span data-ttu-id="07462-124">System. String</span><span class="sxs-lookup"><span data-stu-id="07462-124">System.String</span></span>

## <span data-ttu-id="07462-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07462-125">OUTPUTS</span></span>

### <span data-ttu-id="07462-126">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="07462-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="07462-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="07462-127">NOTES</span></span>

## <span data-ttu-id="07462-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07462-128">RELATED LINKS</span></span>
