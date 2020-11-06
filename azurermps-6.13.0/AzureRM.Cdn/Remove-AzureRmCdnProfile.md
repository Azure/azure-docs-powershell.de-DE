---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498370"
---
# <span data-ttu-id="5b981-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="5b981-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b981-102">SYNOPSIS</span></span>
<span data-ttu-id="5b981-103">Entfernt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="5b981-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b981-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b981-104">SYNTAX</span></span>

### <span data-ttu-id="5b981-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b981-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b981-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b981-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b981-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b981-107">DESCRIPTION</span></span>
<span data-ttu-id="5b981-108">Das Cmdlet **Remove-AzureRmCdnProfile** entfernt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="5b981-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5b981-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b981-109">EXAMPLES</span></span>

## <span data-ttu-id="5b981-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b981-110">PARAMETERS</span></span>

### <span data-ttu-id="5b981-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-111">-CdnProfile</span></span>
<span data-ttu-id="5b981-112">Gibt das von diesem Cmdlet entfernte Profil an.</span><span class="sxs-lookup"><span data-stu-id="5b981-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b981-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-113">-DefaultProfile</span></span>
<span data-ttu-id="5b981-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b981-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b981-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5b981-115">-Force</span></span>
<span data-ttu-id="5b981-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5b981-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b981-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b981-117">-PassThru</span></span>
<span data-ttu-id="5b981-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5b981-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b981-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5b981-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b981-120">-Profilname</span><span class="sxs-lookup"><span data-stu-id="5b981-120">-ProfileName</span></span>
<span data-ttu-id="5b981-121">Gibt den Namen des Profils an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5b981-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b981-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b981-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b981-123">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="5b981-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5b981-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b981-124">-Confirm</span></span>
<span data-ttu-id="5b981-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b981-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b981-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b981-126">-WhatIf</span></span>
<span data-ttu-id="5b981-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b981-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b981-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b981-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b981-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b981-129">CommonParameters</span></span>
<span data-ttu-id="5b981-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b981-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b981-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b981-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b981-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b981-132">INPUTS</span></span>

### <span data-ttu-id="5b981-133">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="5b981-134">Parameter: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b981-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="5b981-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5b981-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b981-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b981-136">OUTPUTS</span></span>

### <span data-ttu-id="5b981-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b981-137">System.Boolean</span></span>

## <span data-ttu-id="5b981-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b981-138">NOTES</span></span>

## <span data-ttu-id="5b981-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b981-139">RELATED LINKS</span></span>

[<span data-ttu-id="5b981-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="5b981-141">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="5b981-142">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b981-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


