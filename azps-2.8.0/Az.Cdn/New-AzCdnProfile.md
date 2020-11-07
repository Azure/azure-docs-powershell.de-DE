---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 7f62d12fbed217fa744ed5753c9234fb0e558caf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652280"
---
# <span data-ttu-id="96f03-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="96f03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96f03-102">SYNOPSIS</span></span>
<span data-ttu-id="96f03-103">Erstellt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="96f03-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="96f03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96f03-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f03-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96f03-105">DESCRIPTION</span></span>
<span data-ttu-id="96f03-106">Das Cmdlet **New-AzCdnProfile** erstellt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="96f03-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="96f03-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96f03-107">EXAMPLES</span></span>

## <span data-ttu-id="96f03-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f03-108">PARAMETERS</span></span>

### <span data-ttu-id="96f03-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-109">-DefaultProfile</span></span>
<span data-ttu-id="96f03-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96f03-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96f03-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="96f03-111">-Location</span></span>
<span data-ttu-id="96f03-112">Gibt den Ressourcen Standort des Profils an.</span><span class="sxs-lookup"><span data-stu-id="96f03-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="96f03-113">-Profilname</span><span class="sxs-lookup"><span data-stu-id="96f03-113">-ProfileName</span></span>
<span data-ttu-id="96f03-114">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="96f03-114">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f03-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f03-115">-ResourceGroupName</span></span>
<span data-ttu-id="96f03-116">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="96f03-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f03-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="96f03-117">-Sku</span></span>
<span data-ttu-id="96f03-118">Gibt die SKU des Profils an.</span><span class="sxs-lookup"><span data-stu-id="96f03-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f03-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="96f03-119">-Tag</span></span>
<span data-ttu-id="96f03-120">Die Tags, die dem Azure CDN-Profil zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96f03-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f03-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96f03-121">-Confirm</span></span>
<span data-ttu-id="96f03-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96f03-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f03-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f03-123">-WhatIf</span></span>
<span data-ttu-id="96f03-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96f03-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f03-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96f03-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f03-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f03-126">CommonParameters</span></span>
<span data-ttu-id="96f03-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f03-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f03-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96f03-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f03-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96f03-129">INPUTS</span></span>

### <span data-ttu-id="96f03-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96f03-130">System.String</span></span>

## <span data-ttu-id="96f03-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96f03-131">OUTPUTS</span></span>

### <span data-ttu-id="96f03-132">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="96f03-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="96f03-133">NOTES</span></span>

## <span data-ttu-id="96f03-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96f03-134">RELATED LINKS</span></span>

[<span data-ttu-id="96f03-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="96f03-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="96f03-137">Satz-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


