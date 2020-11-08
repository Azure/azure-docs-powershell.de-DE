---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179093"
---
# <span data-ttu-id="a54b5-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="a54b5-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="a54b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a54b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a54b5-103">Ruft wichtige Informationen für den Zugriff auf den mit dem Mediendienst verknüpften Ruhe Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="a54b5-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="a54b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a54b5-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a54b5-105">DESCRIPTION</span></span>
<span data-ttu-id="a54b5-106">Das Cmdlet " **Get-AzMediaServiceKey** " ruft wichtige Informationen für den Zugriff auf den dem Azure Media-Dienst zugeordneten Repräsentations Status Transfer (Ruhe)-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="a54b5-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="a54b5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a54b5-107">EXAMPLES</span></span>

### <span data-ttu-id="a54b5-108">Beispiel 1: Abrufen der wichtigsten Informationen für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="a54b5-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="a54b5-109">Dieser Befehl ruft die Schlüsselinformationen für den Zugriff auf den Mediendienst mit dem Namen MediaService001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="a54b5-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="a54b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a54b5-110">PARAMETERS</span></span>

### <span data-ttu-id="a54b5-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a54b5-111">-AccountName</span></span>
<span data-ttu-id="a54b5-112">Gibt den Namen des Medien Diensts an, von dem dieses Cmdlet die Mediendienst Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="a54b5-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="a54b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54b5-113">-DefaultProfile</span></span>
<span data-ttu-id="a54b5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a54b5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="a54b5-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="a54b5-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="a54b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54b5-117">CommonParameters</span></span>
<span data-ttu-id="a54b5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54b5-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54b5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54b5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a54b5-120">INPUTS</span></span>

### <span data-ttu-id="a54b5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a54b5-121">System.String</span></span>

## <span data-ttu-id="a54b5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a54b5-122">OUTPUTS</span></span>

### <span data-ttu-id="a54b5-123">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a54b5-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="a54b5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a54b5-124">NOTES</span></span>

## <span data-ttu-id="a54b5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a54b5-125">RELATED LINKS</span></span>

[<span data-ttu-id="a54b5-126">Satz-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="a54b5-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


