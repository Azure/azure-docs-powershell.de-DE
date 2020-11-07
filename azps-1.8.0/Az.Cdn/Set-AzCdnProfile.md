---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: ecc89a75f144a92653dd0e3c498d664df8c370e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661604"
---
# <span data-ttu-id="1ad6b-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="1ad6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad6b-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="1ad6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ad6b-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ad6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ad6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad6b-106">Das Cmdlet " **Satz-AzCdnProfile** " aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="1ad6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ad6b-107">EXAMPLES</span></span>

## <span data-ttu-id="1ad6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ad6b-108">PARAMETERS</span></span>

### <span data-ttu-id="1ad6b-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-109">-CdnProfile</span></span>
<span data-ttu-id="1ad6b-110">Gibt das Profil an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="1ad6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-111">-DefaultProfile</span></span>
<span data-ttu-id="1ad6b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1ad6b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ad6b-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ad6b-113">-Confirm</span></span>
<span data-ttu-id="1ad6b-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad6b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad6b-115">-WhatIf</span></span>
<span data-ttu-id="1ad6b-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad6b-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad6b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad6b-118">CommonParameters</span></span>
<span data-ttu-id="1ad6b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad6b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad6b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad6b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad6b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ad6b-121">INPUTS</span></span>

### <span data-ttu-id="1ad6b-122">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1ad6b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ad6b-123">OUTPUTS</span></span>

### <span data-ttu-id="1ad6b-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1ad6b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ad6b-125">NOTES</span></span>

## <span data-ttu-id="1ad6b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ad6b-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ad6b-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="1ad6b-128">Neu – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="1ad6b-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6b-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


