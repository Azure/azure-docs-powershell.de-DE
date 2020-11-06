---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481049"
---
# <span data-ttu-id="ca7ae-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ca7ae-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="ca7ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7ae-103">Ruft Informationen zu den Netzwerkzuordnungen der Websitewiederherstellung für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca7ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca7ae-104">SYNTAX</span></span>

### <span data-ttu-id="ca7ae-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca7ae-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca7ae-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="ca7ae-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca7ae-107">DESCRIPTION</span></span>
<span data-ttu-id="ca7ae-108">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrNetworkMapping** " Ruft Informationen zu Azure Site Recovery Network-Zuordnungen für den Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="ca7ae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca7ae-109">EXAMPLES</span></span>

### <span data-ttu-id="ca7ae-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca7ae-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="ca7ae-111">Ruft alle Netz Zuordnungen für das übergebene Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="ca7ae-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca7ae-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="ca7ae-113">Ruft die Netzwerkzuordnung mit dem bereitgestellten Namen in der angegebenen Azure Site Recovery-Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="ca7ae-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca7ae-114">PARAMETERS</span></span>

### <span data-ttu-id="ca7ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7ae-115">-DefaultProfile</span></span>
<span data-ttu-id="ca7ae-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7ae-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca7ae-117">-Name</span></span>
<span data-ttu-id="ca7ae-118">Der Name des abzurufenden ASR-Netzwerk Zuordnungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca7ae-119">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ca7ae-119">-Network</span></span>
<span data-ttu-id="ca7ae-120">Rufen Sie die ASR-Netzwerkzuordnungen ab, die dem angegebenen Netzwerk ASR-Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7ae-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="ca7ae-121">-PrimaryFabric</span></span>
<span data-ttu-id="ca7ae-122">Rufen Sie die ASR-Netzwerkzuordnungen ab, die dem angegebenen primären Fabric-Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7ae-123">CommonParameters</span></span>
<span data-ttu-id="ca7ae-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca7ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7ae-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca7ae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7ae-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca7ae-126">INPUTS</span></span>

### <span data-ttu-id="ca7ae-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ca7ae-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ca7ae-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca7ae-128">OUTPUTS</span></span>

### <span data-ttu-id="ca7ae-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ca7ae-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca7ae-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca7ae-130">NOTES</span></span>

## <span data-ttu-id="ca7ae-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca7ae-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca7ae-132">Neu – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ca7ae-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="ca7ae-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ca7ae-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
