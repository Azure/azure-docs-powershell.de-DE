---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: ac8bc0e8fd65a82f05108351a5b3140da8c1fb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652240"
---
# <span data-ttu-id="abfbf-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="abfbf-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="abfbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="abfbf-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="abfbf-103">Regenerates an account key.</span></span>

## <span data-ttu-id="abfbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abfbf-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abfbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abfbf-105">DESCRIPTION</span></span>
<span data-ttu-id="abfbf-106">Mit dem Cmdlet **New-AzCognitiveServicesAccountKey** wird ein API-Schlüssel für ein Cognitive Services-Konto neu generiert.</span><span class="sxs-lookup"><span data-stu-id="abfbf-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="abfbf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abfbf-107">EXAMPLES</span></span>

### <span data-ttu-id="abfbf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abfbf-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="abfbf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="abfbf-109">PARAMETERS</span></span>

### <span data-ttu-id="abfbf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abfbf-110">-DefaultProfile</span></span>
<span data-ttu-id="abfbf-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="abfbf-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abfbf-112">-Force</span><span class="sxs-lookup"><span data-stu-id="abfbf-112">-Force</span></span>
<span data-ttu-id="abfbf-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="abfbf-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abfbf-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="abfbf-114">-KeyName</span></span>
<span data-ttu-id="abfbf-115">Gibt den Namen des Schlüssels an, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="abfbf-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="abfbf-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="abfbf-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abfbf-117">Key1</span><span class="sxs-lookup"><span data-stu-id="abfbf-117">Key1</span></span>
- <span data-ttu-id="abfbf-118">Key2</span><span class="sxs-lookup"><span data-stu-id="abfbf-118">Key2</span></span>

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

### <span data-ttu-id="abfbf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="abfbf-119">-Name</span></span>
<span data-ttu-id="abfbf-120">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="abfbf-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="abfbf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abfbf-121">-ResourceGroupName</span></span>
<span data-ttu-id="abfbf-122">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="abfbf-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="abfbf-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abfbf-123">-Confirm</span></span>
<span data-ttu-id="abfbf-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abfbf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abfbf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abfbf-125">-WhatIf</span></span>
<span data-ttu-id="abfbf-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abfbf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abfbf-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abfbf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abfbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abfbf-128">CommonParameters</span></span>
<span data-ttu-id="abfbf-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abfbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abfbf-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abfbf-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abfbf-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abfbf-131">INPUTS</span></span>

### <span data-ttu-id="abfbf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="abfbf-132">System.String</span></span>

### <span data-ttu-id="abfbf-133">Microsoft. Azure. Management. CognitiveServices. Models. KeyName</span><span class="sxs-lookup"><span data-stu-id="abfbf-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="abfbf-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abfbf-134">OUTPUTS</span></span>

### <span data-ttu-id="abfbf-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="abfbf-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="abfbf-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="abfbf-136">NOTES</span></span>

## <span data-ttu-id="abfbf-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abfbf-137">RELATED LINKS</span></span>

[<span data-ttu-id="abfbf-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="abfbf-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


