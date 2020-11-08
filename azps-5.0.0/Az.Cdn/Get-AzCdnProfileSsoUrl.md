---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179731"
---
# <span data-ttu-id="265db-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="265db-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="265db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="265db-102">SYNOPSIS</span></span>
<span data-ttu-id="265db-103">Ruft die URL für einmaliges Anmelden eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="265db-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="265db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="265db-104">SYNTAX</span></span>

### <span data-ttu-id="265db-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="265db-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="265db-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="265db-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="265db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="265db-107">DESCRIPTION</span></span>
<span data-ttu-id="265db-108">Das Cmdlet " **Get-AzCdnProfileSsoUrl** " Ruft die URL für einmaliges Anmelden im Azure Content Delivery Network (CDN)-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="265db-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="265db-109">Mit dieser URL können Benutzer eine Verbindung mit einem zusätzlichen Portal herstellen und zusätzliche Features von CDN verwenden.</span><span class="sxs-lookup"><span data-stu-id="265db-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="265db-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="265db-110">EXAMPLES</span></span>

## <span data-ttu-id="265db-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="265db-111">PARAMETERS</span></span>

### <span data-ttu-id="265db-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="265db-112">-CdnProfile</span></span>
<span data-ttu-id="265db-113">Gibt das CDN-Profil an.</span><span class="sxs-lookup"><span data-stu-id="265db-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="265db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265db-114">-DefaultProfile</span></span>
<span data-ttu-id="265db-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="265db-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="265db-116">-Profilname</span><span class="sxs-lookup"><span data-stu-id="265db-116">-ProfileName</span></span>
<span data-ttu-id="265db-117">Gibt den Namen des CDN-Profils an.</span><span class="sxs-lookup"><span data-stu-id="265db-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="265db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265db-118">-ResourceGroupName</span></span>
<span data-ttu-id="265db-119">Gibt den Namen des Ressourcengruppen namens an, zu dem das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="265db-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="265db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265db-120">CommonParameters</span></span>
<span data-ttu-id="265db-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="265db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265db-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="265db-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265db-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="265db-123">INPUTS</span></span>

### <span data-ttu-id="265db-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="265db-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="265db-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="265db-125">OUTPUTS</span></span>

### <span data-ttu-id="265db-126">Microsoft. Azure. Commands. CDN. Models. profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="265db-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="265db-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="265db-127">NOTES</span></span>

## <span data-ttu-id="265db-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="265db-128">RELATED LINKS</span></span>

[<span data-ttu-id="265db-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="265db-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


