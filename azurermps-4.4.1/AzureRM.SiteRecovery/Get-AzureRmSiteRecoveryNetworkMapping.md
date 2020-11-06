---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496841"
---
# <span data-ttu-id="7b8a5-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b8a5-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="7b8a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8a5-103">Ruft Informationen zu den Netzwerkzuordnungen der Websitewiederherstellung für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b8a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b8a5-104">SYNTAX</span></span>

### <span data-ttu-id="7b8a5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b8a5-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8a5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7b8a5-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8a5-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7b8a5-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8a5-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="7b8a5-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8a5-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="7b8a5-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b8a5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b8a5-110">DESCRIPTION</span></span>
<span data-ttu-id="7b8a5-111">Das Cmdlet " **Get-AzureRmSiteRecoveryNetworkMapping** " Ruft Informationen zu Azure Site Recovery-Netzwerkzuordnungen für das aktuelle Standort Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="7b8a5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b8a5-112">EXAMPLES</span></span>

## <span data-ttu-id="7b8a5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b8a5-113">PARAMETERS</span></span>

### <span data-ttu-id="7b8a5-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="7b8a5-114">-Azure</span></span>
<span data-ttu-id="7b8a5-115">Gibt an, dass der Befehl eine Liste der Netzwerkzuordnungen für Netzwerke auf dem primären Server erhält, die Azure virtuellen Netzwerken zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8a5-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7b8a5-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8a5-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="7b8a5-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8a5-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="7b8a5-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8a5-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="7b8a5-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8a5-120">-DefaultProfile</span></span>
<span data-ttu-id="7b8a5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8a5-122">CommonParameters</span></span>
<span data-ttu-id="7b8a5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8a5-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8a5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b8a5-125">INPUTS</span></span>

### <span data-ttu-id="7b8a5-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7b8a5-126">ASRFabric</span></span>
<span data-ttu-id="7b8a5-127">Der Parameter "PrimaryFabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="7b8a5-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="7b8a5-128">ASRServer</span></span>
<span data-ttu-id="7b8a5-129">Der Parameter "PrimaryServer" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b8a5-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="7b8a5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b8a5-130">OUTPUTS</span></span>

### <span data-ttu-id="7b8a5-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="7b8a5-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="7b8a5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b8a5-132">NOTES</span></span>

## <span data-ttu-id="7b8a5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b8a5-133">RELATED LINKS</span></span>

[<span data-ttu-id="7b8a5-134">Neu – AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b8a5-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="7b8a5-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b8a5-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
