---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495758"
---
# <span data-ttu-id="814cd-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="814cd-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="814cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="814cd-102">SYNOPSIS</span></span>
<span data-ttu-id="814cd-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="814cd-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="814cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="814cd-104">SYNTAX</span></span>

### <span data-ttu-id="814cd-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="814cd-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="814cd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="814cd-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="814cd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="814cd-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="814cd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="814cd-108">DESCRIPTION</span></span>
<span data-ttu-id="814cd-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrNetwork** " Ruft Informationen zu Azure Site Recovery Networks für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="814cd-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="814cd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="814cd-110">EXAMPLES</span></span>

### <span data-ttu-id="814cd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="814cd-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="814cd-112">Ruft alle bekannten Netzwerke im angegebenen Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="814cd-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="814cd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="814cd-113">PARAMETERS</span></span>

### <span data-ttu-id="814cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814cd-114">-DefaultProfile</span></span>
<span data-ttu-id="814cd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="814cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="814cd-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="814cd-116">-Fabric</span></span>
<span data-ttu-id="814cd-117">ASR-Fabric-Objekt</span><span class="sxs-lookup"><span data-stu-id="814cd-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="814cd-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="814cd-118">-FriendlyName</span></span>
<span data-ttu-id="814cd-119">Anzeigename des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="814cd-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814cd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="814cd-120">-Name</span></span>
<span data-ttu-id="814cd-121">Name des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="814cd-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814cd-122">CommonParameters</span></span>
<span data-ttu-id="814cd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="814cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814cd-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="814cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814cd-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="814cd-125">INPUTS</span></span>

### <span data-ttu-id="814cd-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="814cd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="814cd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="814cd-127">OUTPUTS</span></span>

### <span data-ttu-id="814cd-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="814cd-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="814cd-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="814cd-129">NOTES</span></span>

## <span data-ttu-id="814cd-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="814cd-130">RELATED LINKS</span></span>
