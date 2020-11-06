---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481513"
---
# <span data-ttu-id="d5219-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d5219-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="d5219-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5219-102">SYNOPSIS</span></span>
<span data-ttu-id="d5219-103">Ruft die Hyper-V-Websites aus dem Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="d5219-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5219-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5219-104">SYNTAX</span></span>

### <span data-ttu-id="d5219-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5219-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5219-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d5219-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5219-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5219-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5219-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5219-108">DESCRIPTION</span></span>
<span data-ttu-id="d5219-109">Das Cmdlet " **Get-AzureRmSiteRecoverySite** " Ruft die Hyper-V-Websites im Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="d5219-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d5219-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5219-110">EXAMPLES</span></span>

## <span data-ttu-id="d5219-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5219-111">PARAMETERS</span></span>

### <span data-ttu-id="d5219-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5219-112">-FriendlyName</span></span>
<span data-ttu-id="d5219-113">Gibt den Anzeigenamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="d5219-113">Specifies the friendly name of the site.</span></span>

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

### <span data-ttu-id="d5219-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d5219-114">-Name</span></span>
<span data-ttu-id="d5219-115">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="d5219-115">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="d5219-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5219-116">-DefaultProfile</span></span>
<span data-ttu-id="d5219-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5219-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5219-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5219-118">CommonParameters</span></span>
<span data-ttu-id="d5219-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5219-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5219-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5219-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5219-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5219-121">INPUTS</span></span>

## <span data-ttu-id="d5219-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5219-122">OUTPUTS</span></span>

### <span data-ttu-id="d5219-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="d5219-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="d5219-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5219-124">NOTES</span></span>

## <span data-ttu-id="d5219-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5219-125">RELATED LINKS</span></span>

[<span data-ttu-id="d5219-126">Neu – AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d5219-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="d5219-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d5219-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
