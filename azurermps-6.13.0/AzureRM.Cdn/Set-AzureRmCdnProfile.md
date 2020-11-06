---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498362"
---
# <span data-ttu-id="76491-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="76491-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="76491-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76491-102">SYNOPSIS</span></span>
<span data-ttu-id="76491-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="76491-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76491-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76491-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76491-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76491-105">DESCRIPTION</span></span>
<span data-ttu-id="76491-106">Das Cmdlet " **Satz-AzureRmCdnProfile** " aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="76491-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="76491-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76491-107">EXAMPLES</span></span>

## <span data-ttu-id="76491-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76491-108">PARAMETERS</span></span>

### <span data-ttu-id="76491-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="76491-109">-CdnProfile</span></span>
<span data-ttu-id="76491-110">Gibt das Profil an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="76491-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76491-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76491-111">-DefaultProfile</span></span>
<span data-ttu-id="76491-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="76491-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76491-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76491-113">-Confirm</span></span>
<span data-ttu-id="76491-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76491-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76491-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76491-115">-WhatIf</span></span>
<span data-ttu-id="76491-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76491-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76491-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76491-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76491-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76491-118">CommonParameters</span></span>
<span data-ttu-id="76491-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76491-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76491-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76491-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76491-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76491-121">INPUTS</span></span>

### <span data-ttu-id="76491-122">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="76491-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="76491-123">Parameter: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76491-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="76491-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76491-124">OUTPUTS</span></span>

### <span data-ttu-id="76491-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="76491-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="76491-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="76491-126">NOTES</span></span>

## <span data-ttu-id="76491-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76491-127">RELATED LINKS</span></span>

[<span data-ttu-id="76491-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="76491-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="76491-129">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="76491-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="76491-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="76491-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


