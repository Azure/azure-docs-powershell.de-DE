---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 506009ac15fa1c9eeeb3e0b7ae902e3c42d1d468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664334"
---
# <span data-ttu-id="8b4bc-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b4bc-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8b4bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4bc-103">Ruft die Details der ASR-Wiederherstellungsdienste-Anbieter ab, die für den Recovery Services Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b4bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b4bc-104">SYNTAX</span></span>

### <span data-ttu-id="8b4bc-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b4bc-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b4bc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b4bc-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b4bc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b4bc-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b4bc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b4bc-108">DESCRIPTION</span></span>
<span data-ttu-id="8b4bc-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrServicesProvider** " Ruft Informationen zu den Azure Site Recovery-Anbietern im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="8b4bc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b4bc-110">EXAMPLES</span></span>

### <span data-ttu-id="8b4bc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b4bc-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="8b4bc-112">Auflisten aller für den Wiederherstellungsdienste-Tresor registrierten ASR-Replikationsdienst Anbieter, die dem angegebenen Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="8b4bc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b4bc-113">PARAMETERS</span></span>

### <span data-ttu-id="8b4bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4bc-114">-DefaultProfile</span></span>
<span data-ttu-id="8b4bc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b4bc-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="8b4bc-116">-Fabric</span></span>
<span data-ttu-id="8b4bc-117">Gibt das ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="8b4bc-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b4bc-118">-FriendlyName</span></span>
<span data-ttu-id="8b4bc-119">Gibt den Anzeigenamen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8b4bc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8b4bc-120">-Name</span></span>
<span data-ttu-id="8b4bc-121">Gibt den Namen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8b4bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4bc-122">CommonParameters</span></span>
<span data-ttu-id="8b4bc-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4bc-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4bc-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b4bc-125">INPUTS</span></span>

### <span data-ttu-id="8b4bc-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8b4bc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8b4bc-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b4bc-127">OUTPUTS</span></span>

### <span data-ttu-id="8b4bc-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8b4bc-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8b4bc-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b4bc-129">NOTES</span></span>

## <span data-ttu-id="8b4bc-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b4bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="8b4bc-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b4bc-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8b4bc-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8b4bc-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
