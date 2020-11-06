---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503865"
---
# <span data-ttu-id="4bcf4-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bcf4-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4bcf4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcf4-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bcf4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bcf4-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bcf4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bcf4-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcf4-106">Das Cmdlet " **Satz-AzureRmCognitiveServicesAccount** " ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="4bcf4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bcf4-107">EXAMPLES</span></span>

## <span data-ttu-id="4bcf4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bcf4-108">PARAMETERS</span></span>

### <span data-ttu-id="4bcf4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcf4-109">-DefaultProfile</span></span>
<span data-ttu-id="4bcf4-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4bcf4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bcf4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4bcf4-111">-Force</span></span>
<span data-ttu-id="4bcf4-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bcf4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4bcf4-113">-Name</span></span>
<span data-ttu-id="4bcf4-114">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-114">Specifies the name of the account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bcf4-116">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4bcf4-117">-SkuName</span></span>
<span data-ttu-id="4bcf4-118">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4bcf4-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4bcf4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bcf4-120">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="4bcf4-120">F0 (free tier)</span></span>
- <span data-ttu-id="4bcf4-121">S0</span><span class="sxs-lookup"><span data-stu-id="4bcf4-121">S0</span></span>
- <span data-ttu-id="4bcf4-122">S1</span><span class="sxs-lookup"><span data-stu-id="4bcf4-122">S1</span></span>
- <span data-ttu-id="4bcf4-123">S2</span><span class="sxs-lookup"><span data-stu-id="4bcf4-123">S2</span></span>
- <span data-ttu-id="4bcf4-124">S3</span><span class="sxs-lookup"><span data-stu-id="4bcf4-124">S3</span></span>
- <span data-ttu-id="4bcf4-125">S4</span><span class="sxs-lookup"><span data-stu-id="4bcf4-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4bcf4-126">-Tag</span></span>
<span data-ttu-id="4bcf4-127">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bcf4-128">-Confirm</span></span>
<span data-ttu-id="4bcf4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcf4-130">-WhatIf</span></span>
<span data-ttu-id="4bcf4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcf4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcf4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcf4-133">CommonParameters</span></span>
<span data-ttu-id="4bcf4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcf4-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcf4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcf4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bcf4-136">INPUTS</span></span>

### <span data-ttu-id="4bcf4-137">Keine</span><span class="sxs-lookup"><span data-stu-id="4bcf4-137">None</span></span>
<span data-ttu-id="4bcf4-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4bcf4-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bcf4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bcf4-139">OUTPUTS</span></span>

### <span data-ttu-id="4bcf4-140">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bcf4-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4bcf4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bcf4-141">NOTES</span></span>

## <span data-ttu-id="4bcf4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bcf4-142">RELATED LINKS</span></span>

[<span data-ttu-id="4bcf4-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bcf4-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4bcf4-144">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bcf4-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4bcf4-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bcf4-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
