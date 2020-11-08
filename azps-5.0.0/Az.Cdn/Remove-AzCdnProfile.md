---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177856"
---
# <span data-ttu-id="f52fa-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="f52fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f52fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f52fa-103">Entfernt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="f52fa-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="f52fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52fa-104">SYNTAX</span></span>

### <span data-ttu-id="f52fa-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f52fa-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f52fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f52fa-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52fa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f52fa-107">DESCRIPTION</span></span>
<span data-ttu-id="f52fa-108">Das Cmdlet **Remove-AzCdnProfile** entfernt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="f52fa-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="f52fa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f52fa-109">EXAMPLES</span></span>

## <span data-ttu-id="f52fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f52fa-110">PARAMETERS</span></span>

### <span data-ttu-id="f52fa-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-111">-CdnProfile</span></span>
<span data-ttu-id="f52fa-112">Gibt das von diesem Cmdlet entfernte Profil an.</span><span class="sxs-lookup"><span data-stu-id="f52fa-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f52fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-113">-DefaultProfile</span></span>
<span data-ttu-id="f52fa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f52fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f52fa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f52fa-115">-Force</span></span>
<span data-ttu-id="f52fa-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f52fa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f52fa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f52fa-117">-PassThru</span></span>
<span data-ttu-id="f52fa-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f52fa-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f52fa-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f52fa-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f52fa-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="f52fa-120">-ProfileName</span></span>
<span data-ttu-id="f52fa-121">Gibt den Namen des Profils an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f52fa-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f52fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="f52fa-123">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="f52fa-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f52fa-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f52fa-124">-Confirm</span></span>
<span data-ttu-id="f52fa-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f52fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52fa-126">-WhatIf</span></span>
<span data-ttu-id="f52fa-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f52fa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52fa-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f52fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52fa-129">CommonParameters</span></span>
<span data-ttu-id="f52fa-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52fa-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f52fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52fa-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f52fa-132">INPUTS</span></span>

### <span data-ttu-id="f52fa-133">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="f52fa-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f52fa-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f52fa-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f52fa-135">OUTPUTS</span></span>

### <span data-ttu-id="f52fa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f52fa-136">System.Boolean</span></span>

## <span data-ttu-id="f52fa-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f52fa-137">NOTES</span></span>

## <span data-ttu-id="f52fa-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f52fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="f52fa-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="f52fa-140">Neu – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="f52fa-141">Satz-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f52fa-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


