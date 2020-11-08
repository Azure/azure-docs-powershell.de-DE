---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177909"
---
# <span data-ttu-id="ecae8-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ecae8-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="ecae8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecae8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecae8-103">Ändert ein Schema des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="ecae8-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="ecae8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecae8-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecae8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecae8-105">DESCRIPTION</span></span>
<span data-ttu-id="ecae8-106">Das Cmdlet " **Satz-AzIntegrationAccountSchema** " ändert ein Schema des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="ecae8-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="ecae8-107">Dieses Cmdlet gibt ein Objekt zurück, das das Schema des Integrations Kontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="ecae8-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="ecae8-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Schemanamen an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="ecae8-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="ecae8-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ecae8-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="ecae8-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ecae8-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="ecae8-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ecae8-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ecae8-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ecae8-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ecae8-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ecae8-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecae8-114">EXAMPLES</span></span>

### <span data-ttu-id="ecae8-115">Beispiel 1: Ändern eines Schemas für ein Integrations Konto</span><span class="sxs-lookup"><span data-stu-id="ecae8-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="ecae8-116">Mit diesem Befehl wird das Schema des Integrations Kontos mit dem Namen IntegrationAccountSchema43 geändert.</span><span class="sxs-lookup"><span data-stu-id="ecae8-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="ecae8-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecae8-117">PARAMETERS</span></span>

### <span data-ttu-id="ecae8-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ecae8-118">-ContentType</span></span>
<span data-ttu-id="ecae8-119">Gibt einen Inhaltstyp für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="ecae8-120">Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="ecae8-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="ecae8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecae8-121">-DefaultProfile</span></span>
<span data-ttu-id="ecae8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ecae8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecae8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ecae8-123">-Force</span></span>
<span data-ttu-id="ecae8-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ecae8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecae8-125">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="ecae8-125">-Metadata</span></span>
<span data-ttu-id="ecae8-126">Gibt ein Metadatenobjekt für das Schema an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="ecae8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ecae8-127">-Name</span></span>
<span data-ttu-id="ecae8-128">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="ecae8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecae8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecae8-130">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ecae8-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="ecae8-131">-SchemaDefinition</span></span>
<span data-ttu-id="ecae8-132">Gibt ein Definitionsobjekt für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="ecae8-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="ecae8-133">-SchemaFilePath</span></span>
<span data-ttu-id="ecae8-134">Gibt den Dateipfad einer Definition für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="ecae8-135">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="ecae8-135">-SchemaName</span></span>
<span data-ttu-id="ecae8-136">Gibt den Namen des Schemas für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="ecae8-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="ecae8-137">-SchemaType</span></span>
<span data-ttu-id="ecae8-138">Gibt den Typ für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecae8-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="ecae8-139">Dieser Parameter unterstützt XML als Typ.</span><span class="sxs-lookup"><span data-stu-id="ecae8-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="ecae8-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecae8-140">-Confirm</span></span>
<span data-ttu-id="ecae8-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecae8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecae8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecae8-142">-WhatIf</span></span>
<span data-ttu-id="ecae8-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecae8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecae8-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecae8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecae8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecae8-145">CommonParameters</span></span>
<span data-ttu-id="ecae8-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecae8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecae8-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecae8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecae8-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecae8-148">INPUTS</span></span>

### <span data-ttu-id="ecae8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ecae8-149">System.String</span></span>

## <span data-ttu-id="ecae8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecae8-150">OUTPUTS</span></span>

### <span data-ttu-id="ecae8-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ecae8-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="ecae8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecae8-152">NOTES</span></span>

## <span data-ttu-id="ecae8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecae8-153">RELATED LINKS</span></span>

[<span data-ttu-id="ecae8-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ecae8-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="ecae8-155">Neu – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ecae8-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="ecae8-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ecae8-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


