---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 8887cdf7da3b69d826bedd4f6de97a8cf39d4a6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470441"
---
# <span data-ttu-id="42dc5-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="42dc5-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="42dc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="42dc5-103">Erstellt ein Integrationskontoschema.</span><span class="sxs-lookup"><span data-stu-id="42dc5-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="42dc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42dc5-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dc5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="42dc5-106">Das **Cmdlet "New-AzIntegrationAccountSchema"** erstellt ein Integrationskontoschema.</span><span class="sxs-lookup"><span data-stu-id="42dc5-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="42dc5-107">Dieses Cmdlet gibt ein Objekt zurück, das das Schema des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="42dc5-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="42dc5-108">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe, den Schemanamen und die Schemadefinition an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="42dc5-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="42dc5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="42dc5-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="42dc5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="42dc5-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="42dc5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="42dc5-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="42dc5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="42dc5-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="42dc5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="42dc5-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42dc5-114">EXAMPLES</span></span>

### <span data-ttu-id="42dc5-115">Beispiel 1: Erstellen des Schemas für das Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="42dc5-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="42dc5-116">Mit diesem Befehl wird das Schema für das Integrationskonto namens "IntegrationAccountSchema1" in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="42dc5-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="42dc5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42dc5-117">PARAMETERS</span></span>

### <span data-ttu-id="42dc5-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="42dc5-118">-ContentType</span></span>
<span data-ttu-id="42dc5-119">Gibt einen Inhaltstyp für das Schema des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="42dc5-120">Dieses Cmdlet unterstützt Anwendung/XML als Karteninhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="42dc5-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="42dc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dc5-121">-DefaultProfile</span></span>
<span data-ttu-id="42dc5-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="42dc5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42dc5-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="42dc5-123">-Metadata</span></span>
<span data-ttu-id="42dc5-124">Gibt ein Metadatenobjekt für das Schema an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-124">Specifies a metadata object for the schema.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="42dc5-125">-Name</span></span>
<span data-ttu-id="42dc5-126">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dc5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dc5-127">-ResourceGroupName</span></span>
<span data-ttu-id="42dc5-128">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="42dc5-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="42dc5-129">-SchemaDefinition</span></span>
<span data-ttu-id="42dc5-130">Gibt ein Definitionsobjekt für das Schema des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="42dc5-131">Geben Sie entweder diesen Parameter oder den *Parameter "SchemaFilePath"* an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="42dc5-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="42dc5-132">-SchemaFilePath</span></span>
<span data-ttu-id="42dc5-133">Gibt den Dateipfad einer Definition für das Schema des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="42dc5-134">Geben Sie entweder diesen Parameter oder den *Parameter SchemaDefinition* an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="42dc5-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="42dc5-135">-SchemaName</span></span>
<span data-ttu-id="42dc5-136">Gibt einen Namen für das Schema des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="42dc5-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="42dc5-137">-SchemaType</span></span>
<span data-ttu-id="42dc5-138">Gibt den Typ für das Schema des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="42dc5-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="42dc5-139">Dieser Parameter unterstützt XML als Typ.</span><span class="sxs-lookup"><span data-stu-id="42dc5-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dc5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42dc5-140">-Confirm</span></span>
<span data-ttu-id="42dc5-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42dc5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dc5-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="42dc5-142">-WhatIf</span></span>
<span data-ttu-id="42dc5-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42dc5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dc5-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42dc5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dc5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dc5-145">CommonParameters</span></span>
<span data-ttu-id="42dc5-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42dc5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dc5-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dc5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dc5-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42dc5-148">INPUTS</span></span>

### <span data-ttu-id="42dc5-149">System.String</span><span class="sxs-lookup"><span data-stu-id="42dc5-149">System.String</span></span>

## <span data-ttu-id="42dc5-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42dc5-150">OUTPUTS</span></span>

### <span data-ttu-id="42dc5-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="42dc5-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="42dc5-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42dc5-152">NOTES</span></span>

## <span data-ttu-id="42dc5-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42dc5-153">RELATED LINKS</span></span>

[<span data-ttu-id="42dc5-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="42dc5-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="42dc5-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="42dc5-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="42dc5-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="42dc5-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


