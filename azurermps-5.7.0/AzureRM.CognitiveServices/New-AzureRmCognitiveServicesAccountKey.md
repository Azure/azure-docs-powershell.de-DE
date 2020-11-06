---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478645"
---
# <span data-ttu-id="a2c48-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2c48-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="a2c48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2c48-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c48-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="a2c48-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2c48-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2c48-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c48-106">Mit dem Cmdlet **New-AzureRmCognitiveServicesAccountKey** wird ein API-Schlüssel für ein Cognitive Services-Konto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="a2c48-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="a2c48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2c48-107">EXAMPLES</span></span>

## <span data-ttu-id="a2c48-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2c48-108">PARAMETERS</span></span>

### <span data-ttu-id="a2c48-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c48-109">-DefaultProfile</span></span>
<span data-ttu-id="a2c48-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2c48-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2c48-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a2c48-111">-Force</span></span>
<span data-ttu-id="a2c48-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a2c48-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2c48-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a2c48-113">-KeyName</span></span>
<span data-ttu-id="a2c48-114">Gibt den Namen des Schlüssels an, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2c48-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="a2c48-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a2c48-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2c48-116">Key1</span><span class="sxs-lookup"><span data-stu-id="a2c48-116">Key1</span></span>
- <span data-ttu-id="a2c48-117">Key2</span><span class="sxs-lookup"><span data-stu-id="a2c48-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c48-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a2c48-118">-Name</span></span>
<span data-ttu-id="a2c48-119">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a2c48-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="a2c48-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c48-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2c48-121">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a2c48-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="a2c48-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2c48-122">-Confirm</span></span>
<span data-ttu-id="a2c48-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2c48-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c48-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c48-124">-WhatIf</span></span>
<span data-ttu-id="a2c48-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2c48-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c48-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2c48-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c48-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c48-127">CommonParameters</span></span>
<span data-ttu-id="a2c48-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c48-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c48-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c48-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c48-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2c48-130">INPUTS</span></span>

### <span data-ttu-id="a2c48-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a2c48-131">None</span></span>
<span data-ttu-id="a2c48-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a2c48-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2c48-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2c48-133">OUTPUTS</span></span>

### <span data-ttu-id="a2c48-134">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a2c48-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="a2c48-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2c48-135">NOTES</span></span>

## <span data-ttu-id="a2c48-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2c48-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2c48-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2c48-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


