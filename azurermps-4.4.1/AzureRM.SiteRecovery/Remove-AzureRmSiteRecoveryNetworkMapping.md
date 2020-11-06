---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 03bd15f1071ac223ba7460c27bcfd9ce96a55dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496834"
---
# <span data-ttu-id="64734-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="64734-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="64734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64734-102">SYNOPSIS</span></span>
<span data-ttu-id="64734-103">Entfernt eine Netzwerkzuordnung aus dem aktuellen Standort Wiederherstellungs Speicher.</span><span class="sxs-lookup"><span data-stu-id="64734-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64734-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64734-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64734-105">DESCRIPTION</span></span>
<span data-ttu-id="64734-106">Das Cmdlet **Remove-AzureRMSiteRecoveryNetworkMapping** entfernt eine Netzwerkzuordnung aus dem aktuellen Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="64734-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="64734-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64734-107">EXAMPLES</span></span>

## <span data-ttu-id="64734-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64734-108">PARAMETERS</span></span>

### <span data-ttu-id="64734-109">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="64734-109">-NetworkMapping</span></span>
<span data-ttu-id="64734-110">Gibt das Netzwerk Zuordnungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="64734-110">Specifies the network mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64734-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64734-111">-DefaultProfile</span></span>
<span data-ttu-id="64734-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64734-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64734-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64734-113">CommonParameters</span></span>
<span data-ttu-id="64734-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64734-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64734-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64734-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64734-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64734-116">INPUTS</span></span>

### <span data-ttu-id="64734-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="64734-117">ASRNetworkMapping</span></span>
<span data-ttu-id="64734-118">Der Parameter "NetworkMapping" akzeptiert den Wert vom Typ "ASRNetworkMapping" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="64734-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="64734-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64734-119">OUTPUTS</span></span>

### <span data-ttu-id="64734-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64734-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64734-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="64734-121">NOTES</span></span>

## <span data-ttu-id="64734-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64734-122">RELATED LINKS</span></span>

[<span data-ttu-id="64734-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="64734-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="64734-124">Neu – AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="64734-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
