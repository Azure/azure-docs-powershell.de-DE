---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009349"
---
# <span data-ttu-id="dae11-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="dae11-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="dae11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dae11-102">SYNOPSIS</span></span>
<span data-ttu-id="dae11-103">Ruft die URL für einmaliges Anmelden eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="dae11-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="dae11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dae11-104">SYNTAX</span></span>

### <span data-ttu-id="dae11-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dae11-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dae11-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae11-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dae11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dae11-107">DESCRIPTION</span></span>
<span data-ttu-id="dae11-108">Das Cmdlet " **Get-AzCdnProfileSsoUrl** " Ruft die URL für einmaliges Anmelden im Azure Content Delivery Network (CDN)-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="dae11-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="dae11-109">Mit dieser URL können Benutzer eine Verbindung mit einem zusätzlichen Portal herstellen und zusätzliche Features von CDN verwenden.</span><span class="sxs-lookup"><span data-stu-id="dae11-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="dae11-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dae11-110">EXAMPLES</span></span>

## <span data-ttu-id="dae11-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dae11-111">PARAMETERS</span></span>

### <span data-ttu-id="dae11-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="dae11-112">-CdnProfile</span></span>
<span data-ttu-id="dae11-113">Gibt das CDN-Profil an.</span><span class="sxs-lookup"><span data-stu-id="dae11-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae11-114">-DefaultProfile</span></span>
<span data-ttu-id="dae11-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dae11-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dae11-116">-Profilname</span><span class="sxs-lookup"><span data-stu-id="dae11-116">-ProfileName</span></span>
<span data-ttu-id="dae11-117">Gibt den Namen des CDN-Profils an.</span><span class="sxs-lookup"><span data-stu-id="dae11-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae11-118">-ResourceGroupName</span></span>
<span data-ttu-id="dae11-119">Gibt den Namen des Ressourcengruppen namens an, zu dem das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="dae11-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae11-120">CommonParameters</span></span>
<span data-ttu-id="dae11-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae11-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dae11-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae11-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dae11-123">INPUTS</span></span>

### <span data-ttu-id="dae11-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="dae11-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="dae11-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dae11-125">OUTPUTS</span></span>

### <span data-ttu-id="dae11-126">Microsoft. Azure. Commands. CDN. Models. profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="dae11-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="dae11-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="dae11-127">NOTES</span></span>

## <span data-ttu-id="dae11-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dae11-128">RELATED LINKS</span></span>

[<span data-ttu-id="dae11-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dae11-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


