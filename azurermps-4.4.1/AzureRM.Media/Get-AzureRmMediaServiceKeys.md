---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665021"
---
# <span data-ttu-id="bd178-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="bd178-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="bd178-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd178-102">SYNOPSIS</span></span>
<span data-ttu-id="bd178-103">Ruft wichtige Informationen für den Zugriff auf den mit dem Mediendienst verknüpften Ruhe Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="bd178-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd178-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd178-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd178-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd178-105">DESCRIPTION</span></span>
<span data-ttu-id="bd178-106">Das Cmdlet " **Get-AzureRmMediaServiceKeys** " ruft wichtige Informationen für den Zugriff auf den dem Azure Media-Dienst zugeordneten Repräsentations Status Transfer (Ruhe)-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="bd178-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="bd178-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd178-107">EXAMPLES</span></span>

### <span data-ttu-id="bd178-108">Beispiel 1: Abrufen der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="bd178-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="bd178-109">Dieser Befehl ruft die Schlüsselinformationen für den Zugriff auf den Mediendienst mit dem Namen MediaService001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="bd178-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="bd178-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd178-110">PARAMETERS</span></span>

### <span data-ttu-id="bd178-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="bd178-111">-AccountName</span></span>
<span data-ttu-id="bd178-112">Gibt den Namen des Medien Diensts an, von dem dieses Cmdlet die Mediendienst Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="bd178-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd178-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd178-113">-ResourceGroupName</span></span>
<span data-ttu-id="bd178-114">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="bd178-114">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd178-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd178-115">-DefaultProfile</span></span>
<span data-ttu-id="bd178-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd178-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd178-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd178-117">CommonParameters</span></span>
<span data-ttu-id="bd178-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd178-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd178-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd178-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd178-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd178-120">INPUTS</span></span>

## <span data-ttu-id="bd178-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd178-121">OUTPUTS</span></span>

### <span data-ttu-id="bd178-122">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="bd178-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="bd178-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd178-123">NOTES</span></span>

## <span data-ttu-id="bd178-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd178-124">RELATED LINKS</span></span>

[<span data-ttu-id="bd178-125">Satz-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="bd178-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


