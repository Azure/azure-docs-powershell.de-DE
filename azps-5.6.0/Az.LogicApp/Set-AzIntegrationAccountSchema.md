---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: cc1c146209758b3ddac9e4b72dcee77e1accf8a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934168"
---
# <span data-ttu-id="61d1b-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61d1b-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="61d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="61d1b-103">Ändert ein Integrationskontoschema.</span><span class="sxs-lookup"><span data-stu-id="61d1b-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="61d1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61d1b-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61d1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="61d1b-106">Das **Cmdlet Set-AzIntegrationAccountSchema** ändert ein Integrationskontoschema.</span><span class="sxs-lookup"><span data-stu-id="61d1b-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="61d1b-107">Dieses Cmdlet gibt ein -Objekt zurück, das das Integrationskontoschema darstellt.</span><span class="sxs-lookup"><span data-stu-id="61d1b-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="61d1b-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Schemanamen an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="61d1b-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="61d1b-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="61d1b-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="61d1b-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61d1b-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="61d1b-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61d1b-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="61d1b-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61d1b-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="61d1b-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61d1b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61d1b-114">EXAMPLES</span></span>

### <span data-ttu-id="61d1b-115">Beispiel 1: Ändern eines Integrationskontoschemas</span><span class="sxs-lookup"><span data-stu-id="61d1b-115">Example 1: Modify an integration account schema</span></span>
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

<span data-ttu-id="61d1b-116">Mit diesem Befehl wird das Integrationskontoschema namens IntegrationAccountSchema43 geändert.</span><span class="sxs-lookup"><span data-stu-id="61d1b-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="61d1b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61d1b-117">PARAMETERS</span></span>

### <span data-ttu-id="61d1b-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="61d1b-118">-ContentType</span></span>
<span data-ttu-id="61d1b-119">Gibt einen Inhaltstyp für das Integrationskontoschema an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="61d1b-120">Dieses Cmdlet unterstützt Application/xml als Karteninhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="61d1b-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="61d1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d1b-121">-DefaultProfile</span></span>
<span data-ttu-id="61d1b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="61d1b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61d1b-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="61d1b-123">-Force</span></span>
<span data-ttu-id="61d1b-124">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="61d1b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61d1b-125">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="61d1b-125">-Metadata</span></span>
<span data-ttu-id="61d1b-126">Gibt ein Metadatenobjekt für das Schema an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="61d1b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="61d1b-127">-Name</span></span>
<span data-ttu-id="61d1b-128">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="61d1b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d1b-129">-ResourceGroupName</span></span>
<span data-ttu-id="61d1b-130">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61d1b-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="61d1b-131">-SchemaDefinition</span></span>
<span data-ttu-id="61d1b-132">Gibt ein Definitionsobjekt für das Integrationskontoschema an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="61d1b-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="61d1b-133">-SchemaFilePath</span></span>
<span data-ttu-id="61d1b-134">Gibt den Dateipfad einer Definition für das Integrationskontoschema an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="61d1b-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="61d1b-135">-SchemaName</span></span>
<span data-ttu-id="61d1b-136">Gibt den Namen des Integrationskontoschemas an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="61d1b-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="61d1b-137">-SchemaType</span></span>
<span data-ttu-id="61d1b-138">Gibt den Typ für das Integrationskontoschema an.</span><span class="sxs-lookup"><span data-stu-id="61d1b-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="61d1b-139">Dieser Parameter unterstützt Xml als Typ.</span><span class="sxs-lookup"><span data-stu-id="61d1b-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="61d1b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61d1b-140">-Confirm</span></span>
<span data-ttu-id="61d1b-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61d1b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d1b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d1b-142">-WhatIf</span></span>
<span data-ttu-id="61d1b-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61d1b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d1b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61d1b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d1b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d1b-145">CommonParameters</span></span>
<span data-ttu-id="61d1b-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d1b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d1b-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d1b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d1b-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61d1b-148">INPUTS</span></span>

### <span data-ttu-id="61d1b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="61d1b-149">System.String</span></span>

## <span data-ttu-id="61d1b-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61d1b-150">OUTPUTS</span></span>

### <span data-ttu-id="61d1b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61d1b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="61d1b-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61d1b-152">NOTES</span></span>

## <span data-ttu-id="61d1b-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61d1b-153">RELATED LINKS</span></span>

[<span data-ttu-id="61d1b-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61d1b-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="61d1b-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61d1b-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="61d1b-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="61d1b-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


