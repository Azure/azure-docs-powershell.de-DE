---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: ad92d2c6a2bcf6dbf9a3bcb75970d3db50adbac0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497598"
---
# <span data-ttu-id="257f1-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257f1-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="257f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="257f1-102">SYNOPSIS</span></span>
<span data-ttu-id="257f1-103">Erstellt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="257f1-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="257f1-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="257f1-105">DESCRIPTION</span></span>
<span data-ttu-id="257f1-106">Das Cmdlet **New-AzureRmIntegrationAccountMap** erstellt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="257f1-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="257f1-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontozuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="257f1-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="257f1-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Kartennamen und die Kartendefinition an.</span><span class="sxs-lookup"><span data-stu-id="257f1-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="257f1-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="257f1-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="257f1-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="257f1-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="257f1-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="257f1-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="257f1-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="257f1-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="257f1-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="257f1-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="257f1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="257f1-114">EXAMPLES</span></span>

### <span data-ttu-id="257f1-115">Beispiel 1: Erstellen einer Integrations Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="257f1-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="257f1-116">Mit diesem Befehl wird die Integrations Kontozuordnung in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="257f1-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="257f1-117">Der Befehl gibt eine Kartendefinition an, die von einem vorherigen Befehl in der $MapContent Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="257f1-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="257f1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="257f1-118">PARAMETERS</span></span>

### <span data-ttu-id="257f1-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="257f1-119">-ContentType</span></span>
<span data-ttu-id="257f1-120">Gibt einen Inhaltstyp für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="257f1-121">Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="257f1-121">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257f1-122">-DefaultProfile</span></span>
<span data-ttu-id="257f1-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="257f1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257f1-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="257f1-124">-MapDefinition</span></span>
<span data-ttu-id="257f1-125">Gibt ein Definitionsobjekt für die Integration-Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="257f1-126">Geben Sie entweder diesen Parameter oder den *MapFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="257f1-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="257f1-127">-MapFilePath</span></span>
<span data-ttu-id="257f1-128">Gibt den Dateipfad einer Definition für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="257f1-129">Geben Sie entweder diesen Parameter oder den *MapDefinition* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="257f1-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="257f1-130">-MapName</span></span>
<span data-ttu-id="257f1-131">Gibt einen Namen für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-131">Specifies a name for the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="257f1-132">-MapType</span></span>
<span data-ttu-id="257f1-133">Gibt den Typ für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="257f1-134">Dieses Cmdlet unterstützt XSLT als Kartentyp.</span><span class="sxs-lookup"><span data-stu-id="257f1-134">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-135">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="257f1-135">-Metadata</span></span>
<span data-ttu-id="257f1-136">Gibt ein Metadatenobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="257f1-136">Specifies a metadata object for the map.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-137">-Name</span><span class="sxs-lookup"><span data-stu-id="257f1-137">-Name</span></span>
<span data-ttu-id="257f1-138">Gibt einen Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="257f1-138">Specifies a name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257f1-139">-ResourceGroupName</span></span>
<span data-ttu-id="257f1-140">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="257f1-140">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f1-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="257f1-141">-Confirm</span></span>
<span data-ttu-id="257f1-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="257f1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257f1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257f1-143">-WhatIf</span></span>
<span data-ttu-id="257f1-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="257f1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257f1-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="257f1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257f1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257f1-146">CommonParameters</span></span>
<span data-ttu-id="257f1-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257f1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257f1-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257f1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257f1-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="257f1-149">INPUTS</span></span>

### <span data-ttu-id="257f1-150">Keine</span><span class="sxs-lookup"><span data-stu-id="257f1-150">None</span></span>
<span data-ttu-id="257f1-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="257f1-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="257f1-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="257f1-152">OUTPUTS</span></span>

### <span data-ttu-id="257f1-153">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257f1-153">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="257f1-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="257f1-154">NOTES</span></span>

## <span data-ttu-id="257f1-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="257f1-155">RELATED LINKS</span></span>

[<span data-ttu-id="257f1-156">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257f1-156">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="257f1-157">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257f1-157">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="257f1-158">Satz-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257f1-158">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


