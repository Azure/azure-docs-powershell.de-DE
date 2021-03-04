---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941960"
---
# <span data-ttu-id="799a4-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="799a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799a4-102">SYNOPSIS</span></span>
<span data-ttu-id="799a4-103">Entfernt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="799a4-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="799a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="799a4-104">SYNTAX</span></span>

### <span data-ttu-id="799a4-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="799a4-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="799a4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="799a4-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799a4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="799a4-107">DESCRIPTION</span></span>
<span data-ttu-id="799a4-108">Das **Cmdlet Remove-AzCdnProfile** entfernt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="799a4-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="799a4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="799a4-109">EXAMPLES</span></span>

## <span data-ttu-id="799a4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="799a4-110">PARAMETERS</span></span>

### <span data-ttu-id="799a4-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-111">-CdnProfile</span></span>
<span data-ttu-id="799a4-112">Gibt das Profil an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="799a4-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="799a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-113">-DefaultProfile</span></span>
<span data-ttu-id="799a4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="799a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="799a4-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="799a4-115">-Force</span></span>
<span data-ttu-id="799a4-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="799a4-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799a4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="799a4-117">-PassThru</span></span>
<span data-ttu-id="799a4-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="799a4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="799a4-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="799a4-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="799a4-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="799a4-120">-ProfileName</span></span>
<span data-ttu-id="799a4-121">Gibt den Namen des Profils an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="799a4-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="799a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="799a4-123">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="799a4-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="799a4-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="799a4-124">-Confirm</span></span>
<span data-ttu-id="799a4-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="799a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799a4-126">-WhatIf</span></span>
<span data-ttu-id="799a4-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="799a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="799a4-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="799a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799a4-129">CommonParameters</span></span>
<span data-ttu-id="799a4-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="799a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799a4-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="799a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799a4-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="799a4-132">INPUTS</span></span>

### <span data-ttu-id="799a4-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="799a4-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="799a4-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="799a4-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="799a4-135">OUTPUTS</span></span>

### <span data-ttu-id="799a4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="799a4-136">System.Boolean</span></span>

## <span data-ttu-id="799a4-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="799a4-137">NOTES</span></span>

## <span data-ttu-id="799a4-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="799a4-138">RELATED LINKS</span></span>

[<span data-ttu-id="799a4-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="799a4-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="799a4-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="799a4-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


