---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476690"
---
# <span data-ttu-id="38590-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="38590-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="38590-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38590-102">SYNOPSIS</span></span>
<span data-ttu-id="38590-103">Löscht die vom Benutzer im aktuellen Kontext festgelegten Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="38590-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38590-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38590-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38590-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38590-105">DESCRIPTION</span></span>
<span data-ttu-id="38590-106">Das Clear-AzureRmDefault-Cmdlet entfernt die vom Benutzer festgelegten Standardeinstellungen, abhängig von den vom Benutzer angegebenen Schalterparametern.</span><span class="sxs-lookup"><span data-stu-id="38590-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="38590-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38590-107">EXAMPLES</span></span>

### <span data-ttu-id="38590-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38590-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="38590-109">Mit diesem Befehl werden alle Standardeinstellungen entfernt, die vom Benutzer im aktuellen Kontext gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="38590-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="38590-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38590-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="38590-111">Dieser Befehl entfernt die vom Benutzer im aktuellen Kontext gesetzte Standardressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="38590-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="38590-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="38590-112">PARAMETERS</span></span>

### <span data-ttu-id="38590-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38590-113">-DefaultProfile</span></span>
<span data-ttu-id="38590-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38590-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38590-115">-Force</span><span class="sxs-lookup"><span data-stu-id="38590-115">-Force</span></span>
<span data-ttu-id="38590-116">Entfernen aller Standardeinstellungen, wenn kein Standardwert angegeben ist</span><span class="sxs-lookup"><span data-stu-id="38590-116">Remove all defaults if no default is specified</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38590-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38590-117">-PassThru</span></span>
<span data-ttu-id="38590-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="38590-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38590-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38590-119">-ResourceGroup</span></span>
<span data-ttu-id="38590-120">Standardressourcen Gruppe löschen</span><span class="sxs-lookup"><span data-stu-id="38590-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38590-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38590-121">-Confirm</span></span>
<span data-ttu-id="38590-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38590-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38590-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38590-123">-WhatIf</span></span>
<span data-ttu-id="38590-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38590-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38590-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38590-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38590-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38590-126">CommonParameters</span></span>
<span data-ttu-id="38590-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38590-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38590-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38590-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38590-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38590-129">INPUTS</span></span>

### <span data-ttu-id="38590-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="38590-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="38590-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38590-131">OUTPUTS</span></span>

### <span data-ttu-id="38590-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="38590-132">System.Object</span></span>

## <span data-ttu-id="38590-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="38590-133">NOTES</span></span>

## <span data-ttu-id="38590-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38590-134">RELATED LINKS</span></span>

