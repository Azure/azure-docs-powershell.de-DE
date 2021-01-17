---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473168"
---
# <span data-ttu-id="14e92-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="14e92-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="14e92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e92-102">SYNOPSIS</span></span>
<span data-ttu-id="14e92-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="14e92-103">Regenerates an account key.</span></span>

## <span data-ttu-id="14e92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14e92-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14e92-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14e92-105">DESCRIPTION</span></span>
<span data-ttu-id="14e92-106">Das **Cmdlet "New-AzCognitiveServicesAccountKey"** generiert einen API-Schlüssel für ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="14e92-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="14e92-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14e92-107">EXAMPLES</span></span>

### <span data-ttu-id="14e92-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14e92-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="14e92-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e92-109">PARAMETERS</span></span>

### <span data-ttu-id="14e92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e92-110">-DefaultProfile</span></span>
<span data-ttu-id="14e92-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="14e92-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14e92-112">-Force</span><span class="sxs-lookup"><span data-stu-id="14e92-112">-Force</span></span>
<span data-ttu-id="14e92-113">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="14e92-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14e92-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="14e92-114">-KeyName</span></span>
<span data-ttu-id="14e92-115">Gibt den Namen des Schlüssels an, der neu generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="14e92-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="14e92-116">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="14e92-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14e92-117">Taste1</span><span class="sxs-lookup"><span data-stu-id="14e92-117">Key1</span></span>
- <span data-ttu-id="14e92-118">Taste2</span><span class="sxs-lookup"><span data-stu-id="14e92-118">Key2</span></span>

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

### <span data-ttu-id="14e92-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14e92-119">-Name</span></span>
<span data-ttu-id="14e92-120">Gibt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="14e92-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="14e92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e92-121">-ResourceGroupName</span></span>
<span data-ttu-id="14e92-122">Gibt den Namen der Ressourcengruppe an, der das Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14e92-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="14e92-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e92-123">-Confirm</span></span>
<span data-ttu-id="14e92-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14e92-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e92-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="14e92-125">-WhatIf</span></span>
<span data-ttu-id="14e92-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14e92-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e92-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14e92-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e92-128">CommonParameters</span></span>
<span data-ttu-id="14e92-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e92-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14e92-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e92-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14e92-131">INPUTS</span></span>

### <span data-ttu-id="14e92-132">System.String</span><span class="sxs-lookup"><span data-stu-id="14e92-132">System.String</span></span>

### <span data-ttu-id="14e92-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="14e92-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="14e92-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14e92-134">OUTPUTS</span></span>

### <span data-ttu-id="14e92-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="14e92-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="14e92-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="14e92-136">NOTES</span></span>

## <span data-ttu-id="14e92-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="14e92-137">RELATED LINKS</span></span>

[<span data-ttu-id="14e92-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="14e92-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


