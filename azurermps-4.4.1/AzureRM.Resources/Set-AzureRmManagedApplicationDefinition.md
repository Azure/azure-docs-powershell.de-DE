---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478957"
---
# <span data-ttu-id="893d4-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="893d4-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="893d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="893d4-102">SYNOPSIS</span></span>
<span data-ttu-id="893d4-103">Aktualisierung der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="893d4-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="893d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="893d4-104">SYNTAX</span></span>

### <span data-ttu-id="893d4-105">Der Parametersatz für verwaltete Anwendungsdefinitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="893d4-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="893d4-106">Standard</span><span class="sxs-lookup"><span data-stu-id="893d4-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="893d4-107">Der Parametersatz der verwalteten Anwendungs Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="893d4-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="893d4-108">DESCRIPTION</span></span>
<span data-ttu-id="893d4-109">Das Cmdlet " **Satz-AzureRmManagedApplicationDefinition** " aktualisiert verwaltete Anwendungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="893d4-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="893d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="893d4-110">EXAMPLES</span></span>

### <span data-ttu-id="893d4-111">Beispiel 1: Aktualisieren der Definitionsbeschreibung für verwaltete Anwendungen</span><span class="sxs-lookup"><span data-stu-id="893d4-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="893d4-112">Dieser Befehl aktualisiert die Definitionsbeschreibung der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="893d4-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="893d4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="893d4-113">PARAMETERS</span></span>

### <span data-ttu-id="893d4-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="893d4-114">-ApiVersion</span></span>
<span data-ttu-id="893d4-115">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="893d4-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="893d4-116">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="893d4-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="893d4-117">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="893d4-117">-Authorization</span></span>
<span data-ttu-id="893d4-118">Die Definitions Autorisierung für verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="893d4-118">The managed application definition authorization.</span></span>
<span data-ttu-id="893d4-119">Durch trennzeichengetrennte Autorisierungs Paare im Format \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="893d4-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893d4-120">-DefaultProfile</span></span>
<span data-ttu-id="893d4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="893d4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893d4-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="893d4-122">-Description</span></span>
<span data-ttu-id="893d4-123">Beschreibung der Definition der verwalteten Anwendung</span><span class="sxs-lookup"><span data-stu-id="893d4-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="893d4-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="893d4-124">-DisplayName</span></span>
<span data-ttu-id="893d4-125">Der Anzeigename der verwalteten Anwendungsdefinition</span><span class="sxs-lookup"><span data-stu-id="893d4-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="893d4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="893d4-126">-Name</span></span>
<span data-ttu-id="893d4-127">Der Definitionsname der verwalteten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="893d4-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d4-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="893d4-128">-PackageFileUri</span></span>
<span data-ttu-id="893d4-129">Der Datei-URI des verwalteten Anwendungs Definitions Pakets.</span><span class="sxs-lookup"><span data-stu-id="893d4-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="893d4-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="893d4-130">-Pre</span></span>
<span data-ttu-id="893d4-131">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="893d4-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="893d4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893d4-132">-ResourceGroupName</span></span>
<span data-ttu-id="893d4-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="893d4-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d4-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="893d4-134">-Tag</span></span>
<span data-ttu-id="893d4-135">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="893d4-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d4-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="893d4-136">-Confirm</span></span>
<span data-ttu-id="893d4-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="893d4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="893d4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893d4-138">-WhatIf</span></span>
<span data-ttu-id="893d4-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893d4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893d4-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="893d4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="893d4-141">-ID</span><span class="sxs-lookup"><span data-stu-id="893d4-141">-Id</span></span>
<span data-ttu-id="893d4-142">Die vollqualifizierte Definitions-ID der verwalteten Anwendung einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="893d4-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="893d4-143">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="893d4-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893d4-144">CommonParameters</span></span>
<span data-ttu-id="893d4-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893d4-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893d4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893d4-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="893d4-147">INPUTS</span></span>

### <span data-ttu-id="893d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="893d4-148">System.String</span></span>
<span data-ttu-id="893d4-149">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="893d4-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="893d4-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="893d4-150">OUTPUTS</span></span>

### <span data-ttu-id="893d4-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="893d4-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="893d4-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="893d4-152">NOTES</span></span>

## <span data-ttu-id="893d4-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="893d4-153">RELATED LINKS</span></span>

