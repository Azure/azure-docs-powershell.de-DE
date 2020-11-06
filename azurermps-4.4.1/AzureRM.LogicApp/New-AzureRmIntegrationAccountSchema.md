---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a9320219e05e61bcd77f15dd526ad45794bd45bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505922"
---
# <span data-ttu-id="78fc0-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="78fc0-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="78fc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="78fc0-103">Erstellt ein Schema für ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="78fc0-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fc0-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78fc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="78fc0-106">Das Cmdlet **New-AzureRmIntegrationAccountSchema** erstellt ein Schema für das Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="78fc0-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="78fc0-107">Dieses Cmdlet gibt ein Objekt zurück, das das Schema des Integrations Kontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="78fc0-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="78fc0-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Schemanamen und die Schema Definition an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>

<span data-ttu-id="78fc0-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="78fc0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="78fc0-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="78fc0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="78fc0-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="78fc0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="78fc0-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="78fc0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="78fc0-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="78fc0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="78fc0-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78fc0-114">EXAMPLES</span></span>

### <span data-ttu-id="78fc0-115">Beispiel 1: Erstellen des Schemas für das Integrations Konto</span><span class="sxs-lookup"><span data-stu-id="78fc0-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="78fc0-116">Mit diesem Befehl wird das Schema des Integrations Kontos mit dem Namen IntegrationAccountSchema1 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="78fc0-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="78fc0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fc0-117">PARAMETERS</span></span>

### <span data-ttu-id="78fc0-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="78fc0-118">-ContentType</span></span>
<span data-ttu-id="78fc0-119">Gibt einen Inhaltstyp für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="78fc0-120">Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="78fc0-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="78fc0-121">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="78fc0-121">-Metadata</span></span>
<span data-ttu-id="78fc0-122">Gibt ein Metadatenobjekt für das Schema an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-122">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="78fc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="78fc0-123">-Name</span></span>
<span data-ttu-id="78fc0-124">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="78fc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="78fc0-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78fc0-127">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="78fc0-127">-SchemaDefinition</span></span>
<span data-ttu-id="78fc0-128">Gibt ein Definitionsobjekt für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-128">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="78fc0-129">Geben Sie entweder diesen Parameter oder den *SchemaFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-129">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="78fc0-130">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="78fc0-130">-SchemaFilePath</span></span>
<span data-ttu-id="78fc0-131">Gibt den Dateipfad einer Definition für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-131">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="78fc0-132">Geben Sie entweder diesen Parameter oder den *SchemaDefinition* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-132">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="78fc0-133">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="78fc0-133">-SchemaName</span></span>
<span data-ttu-id="78fc0-134">Gibt einen Namen für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-134">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="78fc0-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="78fc0-135">-SchemaType</span></span>
<span data-ttu-id="78fc0-136">Gibt den Typ für das Schema des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="78fc0-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="78fc0-137">Dieser Parameter unterstützt XML als Typ.</span><span class="sxs-lookup"><span data-stu-id="78fc0-137">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="78fc0-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78fc0-138">-Confirm</span></span>
<span data-ttu-id="78fc0-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78fc0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78fc0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78fc0-140">-WhatIf</span></span>
<span data-ttu-id="78fc0-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78fc0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78fc0-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78fc0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78fc0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fc0-143">-DefaultProfile</span></span>
<span data-ttu-id="78fc0-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78fc0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78fc0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fc0-145">CommonParameters</span></span>
<span data-ttu-id="78fc0-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fc0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fc0-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fc0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fc0-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78fc0-148">INPUTS</span></span>

## <span data-ttu-id="78fc0-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78fc0-149">OUTPUTS</span></span>

### <span data-ttu-id="78fc0-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="78fc0-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="78fc0-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="78fc0-151">NOTES</span></span>

## <span data-ttu-id="78fc0-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78fc0-152">RELATED LINKS</span></span>

[<span data-ttu-id="78fc0-153">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="78fc0-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="78fc0-154">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="78fc0-154">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="78fc0-155">Satz-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="78fc0-155">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


