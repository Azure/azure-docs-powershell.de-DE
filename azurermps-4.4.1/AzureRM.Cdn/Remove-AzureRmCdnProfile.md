---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497866"
---
# <span data-ttu-id="7fed7-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="7fed7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fed7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fed7-103">Entfernt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="7fed7-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fed7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fed7-104">SYNTAX</span></span>

### <span data-ttu-id="7fed7-105">Parametersatz für fields-Parameter</span><span class="sxs-lookup"><span data-stu-id="7fed7-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fed7-106">Parametersatz für Objektparameter</span><span class="sxs-lookup"><span data-stu-id="7fed7-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fed7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fed7-107">DESCRIPTION</span></span>
<span data-ttu-id="7fed7-108">Das Cmdlet **Remove-AzureRmCdnProfile** entfernt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="7fed7-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="7fed7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fed7-109">EXAMPLES</span></span>

## <span data-ttu-id="7fed7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fed7-110">PARAMETERS</span></span>

### <span data-ttu-id="7fed7-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-111">-CdnProfile</span></span>
<span data-ttu-id="7fed7-112">Gibt das von diesem Cmdlet entfernte Profil an.</span><span class="sxs-lookup"><span data-stu-id="7fed7-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7fed7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7fed7-113">-Force</span></span>
<span data-ttu-id="7fed7-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7fed7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7fed7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fed7-115">-PassThru</span></span>
<span data-ttu-id="7fed7-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7fed7-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7fed7-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7fed7-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7fed7-118">-Profilname</span><span class="sxs-lookup"><span data-stu-id="7fed7-118">-ProfileName</span></span>
<span data-ttu-id="7fed7-119">Gibt den Namen des Profils an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7fed7-119">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7fed7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fed7-120">-ResourceGroupName</span></span>
<span data-ttu-id="7fed7-121">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="7fed7-121">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7fed7-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7fed7-122">-Confirm</span></span>
<span data-ttu-id="7fed7-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fed7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fed7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fed7-124">-WhatIf</span></span>
<span data-ttu-id="7fed7-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7fed7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fed7-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fed7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fed7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-127">-DefaultProfile</span></span>
<span data-ttu-id="7fed7-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fed7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fed7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fed7-129">CommonParameters</span></span>
<span data-ttu-id="7fed7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fed7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fed7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fed7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fed7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fed7-132">INPUTS</span></span>

### <span data-ttu-id="7fed7-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-133">PSProfile</span></span>
<span data-ttu-id="7fed7-134">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7fed7-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="7fed7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fed7-135">OUTPUTS</span></span>

### <span data-ttu-id="7fed7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fed7-136">System.Boolean</span></span>

## <span data-ttu-id="7fed7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fed7-137">NOTES</span></span>

## <span data-ttu-id="7fed7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fed7-138">RELATED LINKS</span></span>

[<span data-ttu-id="7fed7-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="7fed7-140">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="7fed7-141">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7fed7-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


