---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659930"
---
# <span data-ttu-id="faf23-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="faf23-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="faf23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faf23-102">SYNOPSIS</span></span>
<span data-ttu-id="faf23-103">Ruft die Details der ASR-Wiederherstellungsdienste-Anbieter ab, die für den Recovery Services Vault registriert sind.</span><span class="sxs-lookup"><span data-stu-id="faf23-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="faf23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf23-104">SYNTAX</span></span>

### <span data-ttu-id="faf23-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="faf23-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faf23-106">ByName</span><span class="sxs-lookup"><span data-stu-id="faf23-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faf23-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="faf23-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf23-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf23-108">DESCRIPTION</span></span>
<span data-ttu-id="faf23-109">Das Cmdlet " **Get-AzRecoveryServicesAsrServicesProvider** " Ruft Informationen zu den Azure Site Recovery-Anbietern im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="faf23-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="faf23-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf23-110">EXAMPLES</span></span>

### <span data-ttu-id="faf23-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faf23-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="faf23-112">Auflisten aller für den Wiederherstellungsdienste-Tresor registrierten ASR-Replikationsdienst Anbieter, die dem angegebenen Fabric entsprechen.</span><span class="sxs-lookup"><span data-stu-id="faf23-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="faf23-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf23-113">PARAMETERS</span></span>

### <span data-ttu-id="faf23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf23-114">-DefaultProfile</span></span>
<span data-ttu-id="faf23-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faf23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="faf23-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="faf23-116">-Fabric</span></span>
<span data-ttu-id="faf23-117">Gibt das ASR-Fabric-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="faf23-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="faf23-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="faf23-118">-FriendlyName</span></span>
<span data-ttu-id="faf23-119">Gibt den Anzeigenamen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="faf23-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="faf23-120">-Name</span><span class="sxs-lookup"><span data-stu-id="faf23-120">-Name</span></span>
<span data-ttu-id="faf23-121">Gibt den Namen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="faf23-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="faf23-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf23-122">CommonParameters</span></span>
<span data-ttu-id="faf23-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf23-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf23-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf23-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf23-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faf23-125">INPUTS</span></span>

### <span data-ttu-id="faf23-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="faf23-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="faf23-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faf23-127">OUTPUTS</span></span>

### <span data-ttu-id="faf23-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="faf23-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="faf23-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="faf23-129">NOTES</span></span>

## <span data-ttu-id="faf23-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faf23-130">RELATED LINKS</span></span>

[<span data-ttu-id="faf23-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="faf23-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="faf23-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="faf23-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
