---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663835"
---
# <span data-ttu-id="1e3bf-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1e3bf-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1e3bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3bf-103">Erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e3bf-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e3bf-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3bf-106">Das Cmdlet **New-AzureRmPolicySetDefinition** erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="1e3bf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e3bf-107">EXAMPLES</span></span>

### <span data-ttu-id="1e3bf-108">Beispiel 1: Erstellen einer Richtliniensatz Definition mithilfe einer Richtliniensatz Datei</span><span class="sxs-lookup"><span data-stu-id="1e3bf-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="1e3bf-109">Mit diesem Befehl wird eine Richtliniensatz Definition mit dem Namen VMPolicyDefinition erstellt, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="1e3bf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e3bf-110">PARAMETERS</span></span>

### <span data-ttu-id="1e3bf-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e3bf-111">-ApiVersion</span></span>
<span data-ttu-id="1e3bf-112">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1e3bf-113">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3bf-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e3bf-114">-Description</span></span>
<span data-ttu-id="1e3bf-115">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-115">The description for policy set definition.</span></span>

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

### <span data-ttu-id="1e3bf-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1e3bf-116">-DisplayName</span></span>
<span data-ttu-id="1e3bf-117">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-117">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="1e3bf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1e3bf-118">-Name</span></span>
<span data-ttu-id="1e3bf-119">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-119">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3bf-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1e3bf-120">-Parameter</span></span>
<span data-ttu-id="1e3bf-121">Die Parameters-Deklaration für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="1e3bf-122">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="1e3bf-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e3bf-123">-PolicyDefinition</span></span>
<span data-ttu-id="1e3bf-124">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-124">The policy set definition.</span></span> <span data-ttu-id="1e3bf-125">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3bf-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e3bf-126">-Pre</span></span>
<span data-ttu-id="1e3bf-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1e3bf-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e3bf-128">-Confirm</span></span>
<span data-ttu-id="1e3bf-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3bf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3bf-130">-DefaultProfile</span></span>
<span data-ttu-id="1e3bf-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3bf-132">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1e3bf-132">-Metadata</span></span>
<span data-ttu-id="1e3bf-133">Die Metadaten für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-133">The metadata for policy set definition.</span></span> <span data-ttu-id="1e3bf-134">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="1e3bf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3bf-135">-WhatIf</span></span>
<span data-ttu-id="1e3bf-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e3bf-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3bf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3bf-138">CommonParameters</span></span>
<span data-ttu-id="1e3bf-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3bf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3bf-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3bf-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3bf-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e3bf-141">INPUTS</span></span>

### <span data-ttu-id="1e3bf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3bf-142">System.String</span></span>

## <span data-ttu-id="1e3bf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e3bf-143">OUTPUTS</span></span>

### <span data-ttu-id="1e3bf-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1e3bf-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1e3bf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e3bf-145">NOTES</span></span>

## <span data-ttu-id="1e3bf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e3bf-146">RELATED LINKS</span></span>

