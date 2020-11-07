---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 701c7e11a5b76b2071c5810f8c6948c6024eb1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850259"
---
# <span data-ttu-id="1b929-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1b929-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1b929-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b929-102">SYNOPSIS</span></span>
<span data-ttu-id="1b929-103">Erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b929-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b929-104">SYNTAX</span></span>

### <span data-ttu-id="1b929-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b929-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b929-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b929-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b929-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b929-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b929-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b929-108">DESCRIPTION</span></span>
<span data-ttu-id="1b929-109">Das Cmdlet **New-AzureRmPolicySetDefinition** erstellt eine Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-109">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="1b929-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b929-110">EXAMPLES</span></span>

### <span data-ttu-id="1b929-111">Beispiel 1: Erstellen einer Richtliniensatz Definition mithilfe einer Richtliniensatz Datei</span><span class="sxs-lookup"><span data-stu-id="1b929-111">Example 1: Create a policy set definition by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="1b929-112">Mit diesem Befehl wird eine Richtliniensatz Definition mit dem Namen VMPolicyDefinition erstellt, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="1b929-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="1b929-113">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b929-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="1b929-114">Beispiel 2: Erstellen einer parametrisierten Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="1b929-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="1b929-115">Dieser Befehl erstellt eine parametrisierte Richtliniensatz Definition mit dem Namen VMPolicyDefinition, die die in C:\VMPolicy.json angegebenen Richtlinien Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="1b929-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="1b929-116">Der Beispielinhalt der VMPolicy.jsist oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b929-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="1b929-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b929-117">PARAMETERS</span></span>

### <span data-ttu-id="1b929-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b929-118">-ApiVersion</span></span>
<span data-ttu-id="1b929-119">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b929-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b929-120">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1b929-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1b929-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b929-121">-DefaultProfile</span></span>
<span data-ttu-id="1b929-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1b929-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b929-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b929-123">-Description</span></span>
<span data-ttu-id="1b929-124">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="1b929-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b929-125">-DisplayName</span></span>
<span data-ttu-id="1b929-126">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="1b929-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1b929-127">-ManagementGroupName</span></span>
<span data-ttu-id="1b929-128">Der Name der Verwaltungsgruppe der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-128">The name of the management group of the new policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b929-129">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1b929-129">-Metadata</span></span>
<span data-ttu-id="1b929-130">Die Metadaten für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-130">The metadata for policy set definition.</span></span> <span data-ttu-id="1b929-131">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b929-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="1b929-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1b929-132">-Name</span></span>
<span data-ttu-id="1b929-133">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="1b929-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="1b929-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1b929-134">-Parameter</span></span>
<span data-ttu-id="1b929-135">Die Parameters-Deklaration für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="1b929-136">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b929-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="1b929-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1b929-137">-PolicyDefinition</span></span>
<span data-ttu-id="1b929-138">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-138">The policy set definition.</span></span> <span data-ttu-id="1b929-139">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b929-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="1b929-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b929-140">-Pre</span></span>
<span data-ttu-id="1b929-141">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="1b929-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1b929-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1b929-142">-SubscriptionId</span></span>
<span data-ttu-id="1b929-143">Die Abonnement-ID der neuen Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="1b929-143">The subscription ID of the new policy set definition.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b929-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b929-144">-Confirm</span></span>
<span data-ttu-id="1b929-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b929-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b929-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b929-146">-WhatIf</span></span>
<span data-ttu-id="1b929-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b929-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b929-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b929-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b929-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b929-149">CommonParameters</span></span>
<span data-ttu-id="1b929-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b929-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b929-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b929-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b929-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b929-152">INPUTS</span></span>

### <span data-ttu-id="1b929-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1b929-153">System.String</span></span>

### <span data-ttu-id="1b929-154">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1b929-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1b929-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b929-155">OUTPUTS</span></span>

### <span data-ttu-id="1b929-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b929-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b929-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b929-157">NOTES</span></span>

## <span data-ttu-id="1b929-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b929-158">RELATED LINKS</span></span>
