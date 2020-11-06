---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478921"
---
# <span data-ttu-id="8d099-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8d099-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="8d099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d099-102">SYNOPSIS</span></span>
<span data-ttu-id="8d099-103">Erstellt eine Website Wiederherstellungs Website.</span><span class="sxs-lookup"><span data-stu-id="8d099-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d099-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d099-105">DESCRIPTION</span></span>
<span data-ttu-id="8d099-106">Das Cmdlet **New-AzureRmSiteRecoverySite** erstellt eine Azure Site Recovery-Website im aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="8d099-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="8d099-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d099-107">EXAMPLES</span></span>

## <span data-ttu-id="8d099-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d099-108">PARAMETERS</span></span>

### <span data-ttu-id="8d099-109">-Name</span><span class="sxs-lookup"><span data-stu-id="8d099-109">-Name</span></span>
<span data-ttu-id="8d099-110">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="8d099-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d099-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d099-111">-DefaultProfile</span></span>
<span data-ttu-id="8d099-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d099-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d099-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d099-113">CommonParameters</span></span>
<span data-ttu-id="8d099-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d099-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d099-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d099-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d099-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d099-116">INPUTS</span></span>

## <span data-ttu-id="8d099-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d099-117">OUTPUTS</span></span>

## <span data-ttu-id="8d099-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d099-118">NOTES</span></span>

## <span data-ttu-id="8d099-119">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d099-119">RELATED LINKS</span></span>

[<span data-ttu-id="8d099-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8d099-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="8d099-121">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8d099-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
