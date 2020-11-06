---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505222"
---
# <span data-ttu-id="49bce-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="49bce-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="49bce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49bce-102">SYNOPSIS</span></span>
<span data-ttu-id="49bce-103">Ändert ein Konto.</span><span class="sxs-lookup"><span data-stu-id="49bce-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49bce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49bce-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49bce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49bce-105">DESCRIPTION</span></span>
<span data-ttu-id="49bce-106">Das Cmdlet " **Satz-AzureRmCognitiveServicesAccount** " ändert die SKU oder Tags des angegebenen Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="49bce-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="49bce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49bce-107">EXAMPLES</span></span>

## <span data-ttu-id="49bce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49bce-108">PARAMETERS</span></span>

### <span data-ttu-id="49bce-109">-Force</span><span class="sxs-lookup"><span data-stu-id="49bce-109">-Force</span></span>
<span data-ttu-id="49bce-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="49bce-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49bce-111">-Name</span><span class="sxs-lookup"><span data-stu-id="49bce-111">-Name</span></span>
<span data-ttu-id="49bce-112">Gibt den Namen des zu ändernden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="49bce-112">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="49bce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bce-113">-ResourceGroupName</span></span>
<span data-ttu-id="49bce-114">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49bce-114">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="49bce-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="49bce-115">-SkuName</span></span>
<span data-ttu-id="49bce-116">Gibt die SKU für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="49bce-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="49bce-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="49bce-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49bce-118">F0 (﻿Kostenlose Ebene)</span><span class="sxs-lookup"><span data-stu-id="49bce-118">F0 (free tier)</span></span>
- <span data-ttu-id="49bce-119">S0</span><span class="sxs-lookup"><span data-stu-id="49bce-119">S0</span></span>
- <span data-ttu-id="49bce-120">S1</span><span class="sxs-lookup"><span data-stu-id="49bce-120">S1</span></span>
- <span data-ttu-id="49bce-121">S2</span><span class="sxs-lookup"><span data-stu-id="49bce-121">S2</span></span>
- <span data-ttu-id="49bce-122">S3</span><span class="sxs-lookup"><span data-stu-id="49bce-122">S3</span></span>
- <span data-ttu-id="49bce-123">S4</span><span class="sxs-lookup"><span data-stu-id="49bce-123">S4</span></span>

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

### <span data-ttu-id="49bce-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="49bce-124">-Tag</span></span>
<span data-ttu-id="49bce-125">Gibt ein Tag als Name-Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="49bce-125">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="49bce-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49bce-126">-Confirm</span></span>
<span data-ttu-id="49bce-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49bce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bce-128">-WhatIf</span></span>
<span data-ttu-id="49bce-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49bce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49bce-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49bce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bce-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bce-131">-DefaultProfile</span></span>
<span data-ttu-id="49bce-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49bce-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49bce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bce-133">CommonParameters</span></span>
<span data-ttu-id="49bce-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bce-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49bce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bce-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49bce-136">INPUTS</span></span>

## <span data-ttu-id="49bce-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49bce-137">OUTPUTS</span></span>

### <span data-ttu-id="49bce-138">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="49bce-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="49bce-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="49bce-139">NOTES</span></span>

## <span data-ttu-id="49bce-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49bce-140">RELATED LINKS</span></span>

[<span data-ttu-id="49bce-141">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="49bce-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="49bce-142">Neu – AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="49bce-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="49bce-143">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="49bce-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
