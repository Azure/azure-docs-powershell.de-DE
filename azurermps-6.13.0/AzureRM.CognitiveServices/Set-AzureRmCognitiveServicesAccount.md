---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663008"
---
# <span data-ttu-id="948b3-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948b3-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="948b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="948b3-102">SYNOPSIS</span></span>
<span data-ttu-id="948b3-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="948b3-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="948b3-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="948b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="948b3-105">DESCRIPTION</span></span>
<span data-ttu-id="948b3-106">Das Cmdlet " **Satz-AzureRmCognitiveServicesAccount** " ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="948b3-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="948b3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="948b3-107">EXAMPLES</span></span>

### <span data-ttu-id="948b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="948b3-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="948b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="948b3-109">PARAMETERS</span></span>

### <span data-ttu-id="948b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948b3-110">-DefaultProfile</span></span>
<span data-ttu-id="948b3-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="948b3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="948b3-112">-Force</span><span class="sxs-lookup"><span data-stu-id="948b3-112">-Force</span></span>
<span data-ttu-id="948b3-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="948b3-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="948b3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="948b3-114">-Name</span></span>
<span data-ttu-id="948b3-115">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="948b3-115">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="948b3-117">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="948b3-117">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948b3-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="948b3-118">-SkuName</span></span>
<span data-ttu-id="948b3-119">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="948b3-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="948b3-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="948b3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="948b3-121">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="948b3-121">F0 (free tier)</span></span>
- <span data-ttu-id="948b3-122">S0</span><span class="sxs-lookup"><span data-stu-id="948b3-122">S0</span></span>
- <span data-ttu-id="948b3-123">S1</span><span class="sxs-lookup"><span data-stu-id="948b3-123">S1</span></span>
- <span data-ttu-id="948b3-124">S2</span><span class="sxs-lookup"><span data-stu-id="948b3-124">S2</span></span>
- <span data-ttu-id="948b3-125">S3</span><span class="sxs-lookup"><span data-stu-id="948b3-125">S3</span></span>
- <span data-ttu-id="948b3-126">S4</span><span class="sxs-lookup"><span data-stu-id="948b3-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948b3-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="948b3-127">-Tag</span></span>
<span data-ttu-id="948b3-128">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="948b3-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948b3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="948b3-129">-Confirm</span></span>
<span data-ttu-id="948b3-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="948b3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948b3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948b3-131">-WhatIf</span></span>
<span data-ttu-id="948b3-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="948b3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948b3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="948b3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948b3-134">CommonParameters</span></span>
<span data-ttu-id="948b3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948b3-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948b3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948b3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="948b3-137">INPUTS</span></span>

### <span data-ttu-id="948b3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="948b3-138">System.String</span></span>

### <span data-ttu-id="948b3-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="948b3-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="948b3-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="948b3-140">OUTPUTS</span></span>

### <span data-ttu-id="948b3-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948b3-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="948b3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="948b3-142">NOTES</span></span>

## <span data-ttu-id="948b3-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="948b3-143">RELATED LINKS</span></span>

[<span data-ttu-id="948b3-144">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948b3-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="948b3-145">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948b3-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="948b3-146">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="948b3-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
