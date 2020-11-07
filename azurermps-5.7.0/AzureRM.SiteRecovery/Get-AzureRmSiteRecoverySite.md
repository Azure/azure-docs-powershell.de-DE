---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664182"
---
# <span data-ttu-id="8f21b-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8f21b-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="8f21b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f21b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f21b-103">Ruft die Hyper-V-Websites aus dem Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="8f21b-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f21b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f21b-104">SYNTAX</span></span>

### <span data-ttu-id="8f21b-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f21b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f21b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8f21b-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f21b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f21b-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f21b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f21b-108">DESCRIPTION</span></span>
<span data-ttu-id="8f21b-109">Das Cmdlet " **Get-AzureRmSiteRecoverySite** " Ruft die Hyper-V-Websites im Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="8f21b-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8f21b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f21b-110">EXAMPLES</span></span>

## <span data-ttu-id="8f21b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f21b-111">PARAMETERS</span></span>

### <span data-ttu-id="8f21b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f21b-112">-DefaultProfile</span></span>
<span data-ttu-id="8f21b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f21b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f21b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f21b-114">-FriendlyName</span></span>
<span data-ttu-id="8f21b-115">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="8f21b-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f21b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8f21b-116">-Name</span></span>
<span data-ttu-id="8f21b-117">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="8f21b-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f21b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f21b-118">CommonParameters</span></span>
<span data-ttu-id="8f21b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f21b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f21b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f21b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f21b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f21b-121">INPUTS</span></span>

### <span data-ttu-id="8f21b-122">Keine</span><span class="sxs-lookup"><span data-stu-id="8f21b-122">None</span></span>
<span data-ttu-id="8f21b-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8f21b-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f21b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f21b-124">OUTPUTS</span></span>

### <span data-ttu-id="8f21b-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="8f21b-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="8f21b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f21b-126">NOTES</span></span>

## <span data-ttu-id="8f21b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f21b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8f21b-128">Neu – AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8f21b-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="8f21b-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8f21b-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
