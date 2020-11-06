---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479125"
---
# <span data-ttu-id="3dbd9-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="3dbd9-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="3dbd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3dbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbd9-103">Ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie für Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="3dbd9-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dbd9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dbd9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dbd9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dbd9-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbd9-106">Das Cmdlet " **Get-AzureRmApplicationGatewayAvailableSslOptions** " ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie ab</span><span class="sxs-lookup"><span data-stu-id="3dbd9-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="3dbd9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dbd9-107">EXAMPLES</span></span>

### <span data-ttu-id="3dbd9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dbd9-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="3dbd9-109">Diese Befehle gibt alle verfügbaren SSL-Optionen für die SSL-Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="3dbd9-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="3dbd9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dbd9-110">PARAMETERS</span></span>

### <span data-ttu-id="3dbd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbd9-111">-DefaultProfile</span></span>
<span data-ttu-id="3dbd9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3dbd9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dbd9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbd9-113">CommonParameters</span></span>
<span data-ttu-id="3dbd9-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dbd9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbd9-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dbd9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbd9-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3dbd9-116">INPUTS</span></span>

### <span data-ttu-id="3dbd9-117">Keine</span><span class="sxs-lookup"><span data-stu-id="3dbd9-117">None</span></span>

## <span data-ttu-id="3dbd9-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3dbd9-118">OUTPUTS</span></span>

### <span data-ttu-id="3dbd9-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="3dbd9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="3dbd9-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="3dbd9-120">NOTES</span></span>

## <span data-ttu-id="3dbd9-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3dbd9-121">RELATED LINKS</span></span>

