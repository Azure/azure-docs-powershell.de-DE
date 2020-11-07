---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: aacb061772ed1b1202528ebc7b7bc95d725bb9f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664426"
---
# <span data-ttu-id="4a256-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="4a256-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="4a256-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a256-102">SYNOPSIS</span></span>
<span data-ttu-id="4a256-103">Ruft Informationen zu den für den aktuellen Tresor registrierten Website Wiederherstellungsservern ab.</span><span class="sxs-lookup"><span data-stu-id="4a256-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a256-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a256-104">SYNTAX</span></span>

### <span data-ttu-id="4a256-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a256-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a256-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4a256-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a256-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4a256-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a256-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a256-108">DESCRIPTION</span></span>
<span data-ttu-id="4a256-109">Das Cmdlet " **Get-AzureRmSiteRecoveryServer** " Ruft Informationen zu Azure Site Recovery-Servern ab, die für das aktuelle Standort Wiederherstellungs Depot registriert sind.</span><span class="sxs-lookup"><span data-stu-id="4a256-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="4a256-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a256-110">EXAMPLES</span></span>

## <span data-ttu-id="4a256-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a256-111">PARAMETERS</span></span>

### <span data-ttu-id="4a256-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4a256-112">-FriendlyName</span></span>
<span data-ttu-id="4a256-113">Gibt den Anzeigenamen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="4a256-113">Specifies the friendly name of the server.</span></span>

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

### <span data-ttu-id="4a256-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4a256-114">-Name</span></span>
<span data-ttu-id="4a256-115">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="4a256-115">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4a256-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a256-116">-DefaultProfile</span></span>
<span data-ttu-id="4a256-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a256-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a256-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a256-118">CommonParameters</span></span>
<span data-ttu-id="4a256-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a256-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a256-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a256-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a256-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a256-121">INPUTS</span></span>

## <span data-ttu-id="4a256-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a256-122">OUTPUTS</span></span>

### <span data-ttu-id="4a256-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="4a256-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="4a256-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a256-124">NOTES</span></span>

## <span data-ttu-id="4a256-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a256-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a256-126">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="4a256-126">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
