---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478217"
---
# <span data-ttu-id="a9fb6-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a9fb6-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="a9fb6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fb6-103">Ruft Website Wiederherstellungs-Schutzrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fb6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fb6-104">SYNTAX</span></span>

### <span data-ttu-id="a9fb6-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9fb6-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9fb6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a9fb6-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9fb6-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9fb6-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9fb6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9fb6-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fb6-109">Das Cmdlet " **Get-AzureRmSiteRecoveryPolicy** " Ruft die Liste der konfigurierten Azure Site Recovery-Schutzrichtlinien oder einer bestimmten Schutzrichtlinie nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="a9fb6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9fb6-110">EXAMPLES</span></span>

## <span data-ttu-id="a9fb6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fb6-111">PARAMETERS</span></span>

### <span data-ttu-id="a9fb6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fb6-112">-DefaultProfile</span></span>
<span data-ttu-id="a9fb6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9fb6-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a9fb6-114">-FriendlyName</span></span>
<span data-ttu-id="a9fb6-115">Gibt den Anzeigenamen der Replikationsrichtlinie für die Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="a9fb6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a9fb6-116">-Name</span></span>
<span data-ttu-id="a9fb6-117">Gibt den Namen der Replikationsrichtlinie für die Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-117">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="a9fb6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fb6-118">CommonParameters</span></span>
<span data-ttu-id="a9fb6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fb6-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fb6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fb6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9fb6-121">INPUTS</span></span>

### <span data-ttu-id="a9fb6-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a9fb6-122">None</span></span>
<span data-ttu-id="a9fb6-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a9fb6-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9fb6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9fb6-124">OUTPUTS</span></span>

### <span data-ttu-id="a9fb6-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="a9fb6-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="a9fb6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9fb6-126">NOTES</span></span>

## <span data-ttu-id="a9fb6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9fb6-127">RELATED LINKS</span></span>

[<span data-ttu-id="a9fb6-128">Neu – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a9fb6-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="a9fb6-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a9fb6-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
