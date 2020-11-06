---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500670"
---
# <span data-ttu-id="ed42e-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ed42e-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="ed42e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed42e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed42e-103">Aktualisiert einen Website Wiederherstellungsserver.</span><span class="sxs-lookup"><span data-stu-id="ed42e-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed42e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed42e-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed42e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed42e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed42e-106">Das Cmdlet **Update-AzureRmSiteRecoveryServer** aktualisiert einen Azure Site Recovery-Server.</span><span class="sxs-lookup"><span data-stu-id="ed42e-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="ed42e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed42e-107">EXAMPLES</span></span>

## <span data-ttu-id="ed42e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed42e-108">PARAMETERS</span></span>

### <span data-ttu-id="ed42e-109">-Server</span><span class="sxs-lookup"><span data-stu-id="ed42e-109">-Server</span></span>
<span data-ttu-id="ed42e-110">Gibt den Standort Wiederherstellungsserver an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ed42e-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed42e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed42e-111">-DefaultProfile</span></span>
<span data-ttu-id="ed42e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed42e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed42e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed42e-113">CommonParameters</span></span>
<span data-ttu-id="ed42e-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed42e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed42e-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed42e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed42e-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed42e-116">INPUTS</span></span>

### <span data-ttu-id="ed42e-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="ed42e-117">ASRServer</span></span>
<span data-ttu-id="ed42e-118">Der Parameter "Server" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed42e-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="ed42e-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed42e-119">OUTPUTS</span></span>

## <span data-ttu-id="ed42e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed42e-120">NOTES</span></span>

## <span data-ttu-id="ed42e-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed42e-121">RELATED LINKS</span></span>

[<span data-ttu-id="ed42e-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ed42e-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="ed42e-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ed42e-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
