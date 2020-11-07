---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661593"
---
# <span data-ttu-id="cdede-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cdede-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="cdede-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdede-102">SYNOPSIS</span></span>
<span data-ttu-id="cdede-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="cdede-103">Modifies an account.</span></span>

## <span data-ttu-id="cdede-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdede-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdede-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdede-105">DESCRIPTION</span></span>
<span data-ttu-id="cdede-106">Das Cmdlet " **Satz-AzCognitiveServicesAccount** " ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="cdede-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="cdede-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdede-107">EXAMPLES</span></span>

### <span data-ttu-id="cdede-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdede-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="cdede-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdede-109">PARAMETERS</span></span>

### <span data-ttu-id="cdede-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdede-110">-DefaultProfile</span></span>
<span data-ttu-id="cdede-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cdede-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdede-112">-Force</span><span class="sxs-lookup"><span data-stu-id="cdede-112">-Force</span></span>
<span data-ttu-id="cdede-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cdede-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdede-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cdede-114">-Name</span></span>
<span data-ttu-id="cdede-115">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="cdede-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="cdede-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdede-116">-ResourceGroupName</span></span>
<span data-ttu-id="cdede-117">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cdede-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="cdede-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cdede-118">-SkuName</span></span>
<span data-ttu-id="cdede-119">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="cdede-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="cdede-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cdede-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cdede-121">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="cdede-121">F0 (free tier)</span></span>
- <span data-ttu-id="cdede-122">S0</span><span class="sxs-lookup"><span data-stu-id="cdede-122">S0</span></span>
- <span data-ttu-id="cdede-123">S1</span><span class="sxs-lookup"><span data-stu-id="cdede-123">S1</span></span>
- <span data-ttu-id="cdede-124">S2</span><span class="sxs-lookup"><span data-stu-id="cdede-124">S2</span></span>
- <span data-ttu-id="cdede-125">S3</span><span class="sxs-lookup"><span data-stu-id="cdede-125">S3</span></span>
- <span data-ttu-id="cdede-126">S4</span><span class="sxs-lookup"><span data-stu-id="cdede-126">S4</span></span>

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

### <span data-ttu-id="cdede-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="cdede-127">-Tag</span></span>
<span data-ttu-id="cdede-128">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="cdede-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="cdede-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdede-129">-Confirm</span></span>
<span data-ttu-id="cdede-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdede-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdede-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdede-131">-WhatIf</span></span>
<span data-ttu-id="cdede-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdede-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdede-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdede-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdede-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdede-134">CommonParameters</span></span>
<span data-ttu-id="cdede-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdede-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdede-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdede-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdede-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdede-137">INPUTS</span></span>

### <span data-ttu-id="cdede-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cdede-138">System.String</span></span>

### <span data-ttu-id="cdede-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="cdede-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="cdede-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdede-140">OUTPUTS</span></span>

### <span data-ttu-id="cdede-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cdede-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="cdede-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdede-142">NOTES</span></span>

## <span data-ttu-id="cdede-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdede-143">RELATED LINKS</span></span>

[<span data-ttu-id="cdede-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cdede-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="cdede-145">Neu – AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cdede-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="cdede-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cdede-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
