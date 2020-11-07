---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664178"
---
# <span data-ttu-id="e8f1d-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e8f1d-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="e8f1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f1d-103">Ruft Website-Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8f1d-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f1d-106">Das Cmdlet " **Get-AzureRmSiteRecoveryVault** " Ruft eine Liste der Azure Site Recovery Vaults oder eines bestimmten Standort Wiederherstellungs Depots aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="e8f1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8f1d-107">EXAMPLES</span></span>

## <span data-ttu-id="e8f1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8f1d-108">PARAMETERS</span></span>

### <span data-ttu-id="e8f1d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f1d-109">-DefaultProfile</span></span>
<span data-ttu-id="e8f1d-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f1d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="e8f1d-111">-Name</span></span>
<span data-ttu-id="e8f1d-112">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="e8f1d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f1d-113">-ResourceGroupName</span></span>
<span data-ttu-id="e8f1d-114">Gibt den Namen der Azure-Ressourcengruppe an, aus der das Wiederherstellungsdienste-Objekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

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

### <span data-ttu-id="e8f1d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f1d-115">CommonParameters</span></span>
<span data-ttu-id="e8f1d-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f1d-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f1d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f1d-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8f1d-118">INPUTS</span></span>

### <span data-ttu-id="e8f1d-119">Keine</span><span class="sxs-lookup"><span data-stu-id="e8f1d-119">None</span></span>
<span data-ttu-id="e8f1d-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e8f1d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8f1d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8f1d-121">OUTPUTS</span></span>

### <span data-ttu-id="e8f1d-122">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="e8f1d-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="e8f1d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8f1d-123">NOTES</span></span>

## <span data-ttu-id="e8f1d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8f1d-124">RELATED LINKS</span></span>

[<span data-ttu-id="e8f1d-125">Neu – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e8f1d-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="e8f1d-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e8f1d-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
