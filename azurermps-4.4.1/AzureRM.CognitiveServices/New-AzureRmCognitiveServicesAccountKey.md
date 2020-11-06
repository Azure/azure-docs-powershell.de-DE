---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505234"
---
# <span data-ttu-id="24608-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="24608-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="24608-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24608-102">SYNOPSIS</span></span>
<span data-ttu-id="24608-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="24608-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24608-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24608-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24608-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24608-105">DESCRIPTION</span></span>
<span data-ttu-id="24608-106">Mit dem Cmdlet **New-AzureRmCognitiveServicesAccountKey** wird ein API-Schlüssel für ein Cognitive Services-Konto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="24608-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="24608-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24608-107">EXAMPLES</span></span>

## <span data-ttu-id="24608-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="24608-108">PARAMETERS</span></span>

### <span data-ttu-id="24608-109">-Force</span><span class="sxs-lookup"><span data-stu-id="24608-109">-Force</span></span>
<span data-ttu-id="24608-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="24608-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24608-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="24608-111">-KeyName</span></span>
<span data-ttu-id="24608-112">Gibt den Namen des Schlüssels an, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="24608-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="24608-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="24608-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24608-114">Key1</span><span class="sxs-lookup"><span data-stu-id="24608-114">Key1</span></span>
- <span data-ttu-id="24608-115">Key2</span><span class="sxs-lookup"><span data-stu-id="24608-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24608-116">-Name</span><span class="sxs-lookup"><span data-stu-id="24608-116">-Name</span></span>
<span data-ttu-id="24608-117">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="24608-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="24608-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24608-118">-ResourceGroupName</span></span>
<span data-ttu-id="24608-119">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="24608-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="24608-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24608-120">-Confirm</span></span>
<span data-ttu-id="24608-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24608-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24608-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24608-122">-WhatIf</span></span>
<span data-ttu-id="24608-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24608-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24608-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24608-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24608-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24608-125">-DefaultProfile</span></span>
<span data-ttu-id="24608-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24608-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24608-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24608-127">CommonParameters</span></span>
<span data-ttu-id="24608-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24608-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24608-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24608-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24608-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24608-130">INPUTS</span></span>

## <span data-ttu-id="24608-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24608-131">OUTPUTS</span></span>

### <span data-ttu-id="24608-132">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="24608-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="24608-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="24608-133">NOTES</span></span>

## <span data-ttu-id="24608-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24608-134">RELATED LINKS</span></span>

[<span data-ttu-id="24608-135">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="24608-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


