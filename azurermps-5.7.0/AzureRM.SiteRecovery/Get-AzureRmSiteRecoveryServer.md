---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664185"
---
# <span data-ttu-id="49039-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="49039-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="49039-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49039-102">SYNOPSIS</span></span>
<span data-ttu-id="49039-103">Ruft Informationen zu den für den aktuellen Tresor registrierten Website Wiederherstellungsservern ab.</span><span class="sxs-lookup"><span data-stu-id="49039-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49039-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49039-104">SYNTAX</span></span>

### <span data-ttu-id="49039-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="49039-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49039-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49039-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49039-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="49039-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49039-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49039-108">DESCRIPTION</span></span>
<span data-ttu-id="49039-109">Das Cmdlet " **Get-AzureRmSiteRecoveryServer** " Ruft Informationen zu Azure Site Recovery-Servern ab, die für das aktuelle Standort Wiederherstellungs Depot registriert sind.</span><span class="sxs-lookup"><span data-stu-id="49039-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="49039-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49039-110">EXAMPLES</span></span>

## <span data-ttu-id="49039-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="49039-111">PARAMETERS</span></span>

### <span data-ttu-id="49039-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49039-112">-DefaultProfile</span></span>
<span data-ttu-id="49039-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49039-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49039-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="49039-114">-FriendlyName</span></span>
<span data-ttu-id="49039-115">Gibt den Anzeigenamen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="49039-115">Specifies the friendly name of the server.</span></span>

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

### <span data-ttu-id="49039-116">-Name</span><span class="sxs-lookup"><span data-stu-id="49039-116">-Name</span></span>
<span data-ttu-id="49039-117">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="49039-117">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="49039-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49039-118">CommonParameters</span></span>
<span data-ttu-id="49039-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49039-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49039-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49039-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49039-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49039-121">INPUTS</span></span>

### <span data-ttu-id="49039-122">Keine</span><span class="sxs-lookup"><span data-stu-id="49039-122">None</span></span>
<span data-ttu-id="49039-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="49039-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49039-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49039-124">OUTPUTS</span></span>

### <span data-ttu-id="49039-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="49039-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="49039-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="49039-126">NOTES</span></span>

## <span data-ttu-id="49039-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49039-127">RELATED LINKS</span></span>

[<span data-ttu-id="49039-128">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="49039-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
