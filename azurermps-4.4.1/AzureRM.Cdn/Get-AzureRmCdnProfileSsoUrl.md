---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663610"
---
# <span data-ttu-id="dc1ba-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="dc1ba-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="dc1ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1ba-103">Ruft die URL für einmaliges Anmelden eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc1ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc1ba-104">SYNTAX</span></span>

### <span data-ttu-id="dc1ba-105">Parametersatz für fields-Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc1ba-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc1ba-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="dc1ba-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc1ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc1ba-107">DESCRIPTION</span></span>
<span data-ttu-id="dc1ba-108">Das Cmdlet " **Get-AzureRmCdnProfileSsoUrl** " Ruft die URL für einmaliges Anmelden im Azure Content Delivery Network (CDN)-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="dc1ba-109">Diese URL ermöglicht es Benutzern, conntect zu einem zusätzlichen Portal zu verwenden und zusätzliche Features von CDN zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="dc1ba-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc1ba-110">EXAMPLES</span></span>

## <span data-ttu-id="dc1ba-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc1ba-111">PARAMETERS</span></span>

### <span data-ttu-id="dc1ba-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc1ba-112">-CdnProfile</span></span>
<span data-ttu-id="dc1ba-113">Gibt das CDN-Profil an.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc1ba-114">-Profilname</span><span class="sxs-lookup"><span data-stu-id="dc1ba-114">-ProfileName</span></span>
<span data-ttu-id="dc1ba-115">Gibt den Namen des CDN-Profils an.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1ba-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1ba-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc1ba-117">Gibt den Namen des Ressourcengruppen namens an, zu dem das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1ba-118">-DefaultProfile</span></span>
<span data-ttu-id="dc1ba-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc1ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1ba-120">CommonParameters</span></span>
<span data-ttu-id="dc1ba-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1ba-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1ba-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1ba-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc1ba-123">INPUTS</span></span>

### <span data-ttu-id="dc1ba-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="dc1ba-124">PSProfile</span></span>
<span data-ttu-id="dc1ba-125">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="dc1ba-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc1ba-126">OUTPUTS</span></span>

###  
<span data-ttu-id="dc1ba-127">Dieses Cmdlet gibt eine URL zurück.</span><span class="sxs-lookup"><span data-stu-id="dc1ba-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="dc1ba-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc1ba-128">NOTES</span></span>

## <span data-ttu-id="dc1ba-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc1ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc1ba-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dc1ba-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


