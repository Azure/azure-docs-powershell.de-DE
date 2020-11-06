---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496490"
---
# <span data-ttu-id="b4084-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b4084-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="b4084-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4084-102">SYNOPSIS</span></span>
<span data-ttu-id="b4084-103">Ruft wichtige Informationen für den Zugriff auf den mit dem Mediendienst verknüpften Ruhe Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="b4084-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4084-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4084-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4084-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4084-105">DESCRIPTION</span></span>
<span data-ttu-id="b4084-106">Das Cmdlet " **Get-AzureRmMediaServiceKeys** " ruft wichtige Informationen für den Zugriff auf den dem Azure Media-Dienst zugeordneten Repräsentations Status Transfer (Ruhe)-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="b4084-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="b4084-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4084-107">EXAMPLES</span></span>

### <span data-ttu-id="b4084-108">Beispiel 1: Abrufen der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="b4084-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="b4084-109">Dieser Befehl ruft die Schlüsselinformationen für den Zugriff auf den Mediendienst mit dem Namen MediaService001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="b4084-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="b4084-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4084-110">PARAMETERS</span></span>

### <span data-ttu-id="b4084-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b4084-111">-AccountName</span></span>
<span data-ttu-id="b4084-112">Gibt den Namen des Medien Diensts an, von dem dieses Cmdlet die Mediendienst Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="b4084-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4084-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4084-113">-DefaultProfile</span></span>
<span data-ttu-id="b4084-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b4084-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4084-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4084-115">-ResourceGroupName</span></span>
<span data-ttu-id="b4084-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="b4084-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4084-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4084-117">CommonParameters</span></span>
<span data-ttu-id="b4084-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4084-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4084-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4084-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4084-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4084-120">INPUTS</span></span>

### <span data-ttu-id="b4084-121">Keine</span><span class="sxs-lookup"><span data-stu-id="b4084-121">None</span></span>
<span data-ttu-id="b4084-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b4084-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4084-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4084-123">OUTPUTS</span></span>

### <span data-ttu-id="b4084-124">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b4084-124">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="b4084-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4084-125">NOTES</span></span>

## <span data-ttu-id="b4084-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4084-126">RELATED LINKS</span></span>

[<span data-ttu-id="b4084-127">Satz-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="b4084-127">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


