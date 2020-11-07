---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663822"
---
# <span data-ttu-id="aa932-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="aa932-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="aa932-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa932-102">SYNOPSIS</span></span>
<span data-ttu-id="aa932-103">Ruft Website-Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="aa932-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa932-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa932-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa932-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa932-105">DESCRIPTION</span></span>
<span data-ttu-id="aa932-106">Das Cmdlet " **Get-AzureRmSiteRecoveryVault** " Ruft eine Liste der Azure Site Recovery Vaults oder eines bestimmten Standort Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="aa932-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="aa932-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa932-107">EXAMPLES</span></span>

## <span data-ttu-id="aa932-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa932-108">PARAMETERS</span></span>

### <span data-ttu-id="aa932-109">-Name</span><span class="sxs-lookup"><span data-stu-id="aa932-109">-Name</span></span>
<span data-ttu-id="aa932-110">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="aa932-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa932-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa932-111">-ResourceGroupName</span></span>
<span data-ttu-id="aa932-112">Gibt den Namen der Azure-Ressourcengruppe an, aus der das Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa932-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa932-113">-DefaultProfile</span></span>
<span data-ttu-id="aa932-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa932-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa932-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa932-115">CommonParameters</span></span>
<span data-ttu-id="aa932-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa932-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa932-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa932-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa932-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa932-118">INPUTS</span></span>

## <span data-ttu-id="aa932-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa932-119">OUTPUTS</span></span>

### <span data-ttu-id="aa932-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="aa932-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="aa932-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa932-121">NOTES</span></span>

## <span data-ttu-id="aa932-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa932-122">RELATED LINKS</span></span>

[<span data-ttu-id="aa932-123">Neu – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="aa932-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="aa932-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="aa932-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
