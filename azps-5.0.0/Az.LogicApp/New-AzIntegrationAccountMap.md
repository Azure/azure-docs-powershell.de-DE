---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180351"
---
# <span data-ttu-id="3319d-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3319d-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="3319d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3319d-102">SYNOPSIS</span></span>
<span data-ttu-id="3319d-103">Erstellt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="3319d-103">Creates an integration account map.</span></span>

## <span data-ttu-id="3319d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3319d-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3319d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3319d-105">DESCRIPTION</span></span>
<span data-ttu-id="3319d-106">Das Cmdlet **New-AzIntegrationAccountMap** erstellt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="3319d-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="3319d-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontozuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="3319d-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="3319d-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Kartennamen und die Kartendefinition an.</span><span class="sxs-lookup"><span data-stu-id="3319d-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="3319d-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="3319d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="3319d-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3319d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3319d-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3319d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3319d-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3319d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3319d-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3319d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3319d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3319d-114">EXAMPLES</span></span>

### <span data-ttu-id="3319d-115">Beispiel 1: Erstellen einer Integrations Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="3319d-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="3319d-116">Mit diesem Befehl wird die Integrations Kontozuordnung in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="3319d-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="3319d-117">Der Befehl gibt eine Kartendefinition an, die von einem vorherigen Befehl in der $MapContent Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3319d-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="3319d-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3319d-118">Example 2</span></span>

<span data-ttu-id="3319d-119">Erstellt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="3319d-119">Creates an integration account map.</span></span> <span data-ttu-id="3319d-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="3319d-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="3319d-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="3319d-121">PARAMETERS</span></span>

### <span data-ttu-id="3319d-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="3319d-122">-ContentType</span></span>
<span data-ttu-id="3319d-123">Gibt einen Inhaltstyp für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="3319d-124">Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="3319d-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="3319d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3319d-125">-DefaultProfile</span></span>
<span data-ttu-id="3319d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3319d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3319d-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="3319d-127">-MapDefinition</span></span>
<span data-ttu-id="3319d-128">Gibt ein Definitionsobjekt für die Integration-Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="3319d-129">Geben Sie entweder diesen Parameter oder den *MapFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="3319d-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="3319d-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="3319d-130">-MapFilePath</span></span>
<span data-ttu-id="3319d-131">Gibt den Dateipfad einer Definition für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="3319d-132">Geben Sie entweder diesen Parameter oder den *MapDefinition* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="3319d-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="3319d-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="3319d-133">-MapName</span></span>
<span data-ttu-id="3319d-134">Gibt einen Namen für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="3319d-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="3319d-135">-MapType</span></span>
<span data-ttu-id="3319d-136">Gibt den Typ für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="3319d-137">Dieses Cmdlet unterstützt XSLT als Kartentyp.</span><span class="sxs-lookup"><span data-stu-id="3319d-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319d-138">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="3319d-138">-Metadata</span></span>
<span data-ttu-id="3319d-139">Gibt ein Metadatenobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3319d-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="3319d-140">-Name</span><span class="sxs-lookup"><span data-stu-id="3319d-140">-Name</span></span>
<span data-ttu-id="3319d-141">Gibt einen Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="3319d-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="3319d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3319d-142">-ResourceGroupName</span></span>
<span data-ttu-id="3319d-143">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3319d-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3319d-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3319d-144">-Confirm</span></span>
<span data-ttu-id="3319d-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3319d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3319d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3319d-146">-WhatIf</span></span>
<span data-ttu-id="3319d-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3319d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3319d-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3319d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3319d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3319d-149">CommonParameters</span></span>
<span data-ttu-id="3319d-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3319d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3319d-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3319d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3319d-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3319d-152">INPUTS</span></span>

### <span data-ttu-id="3319d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3319d-153">System.String</span></span>

## <span data-ttu-id="3319d-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3319d-154">OUTPUTS</span></span>

### <span data-ttu-id="3319d-155">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3319d-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="3319d-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="3319d-156">NOTES</span></span>

## <span data-ttu-id="3319d-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3319d-157">RELATED LINKS</span></span>

[<span data-ttu-id="3319d-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3319d-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="3319d-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3319d-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="3319d-160">Satz-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3319d-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


