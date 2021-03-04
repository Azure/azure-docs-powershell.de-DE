---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 7ce86f893cbead5b2c5ac7a57af44eeb7f92f9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921960"
---
# <span data-ttu-id="fccb5-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="fccb5-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="fccb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fccb5-102">SYNOPSIS</span></span>
<span data-ttu-id="fccb5-103">Erstellt eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="fccb5-103">Creates an integration account map.</span></span>

## <span data-ttu-id="fccb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fccb5-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fccb5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fccb5-105">DESCRIPTION</span></span>
<span data-ttu-id="fccb5-106">Das **Cmdlet New-AzIntegrationAccountMap** erstellt eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="fccb5-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="fccb5-107">Dieses Cmdlet gibt ein -Objekt zurück, das die Integrationskontozuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="fccb5-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="fccb5-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen, den Kartennamen und die Kartendefinition an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="fccb5-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="fccb5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="fccb5-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="fccb5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fccb5-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="fccb5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fccb5-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="fccb5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fccb5-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="fccb5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fccb5-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fccb5-114">EXAMPLES</span></span>

### <span data-ttu-id="fccb5-115">Beispiel 1: Erstellen einer Integrationskontozuordnung</span><span class="sxs-lookup"><span data-stu-id="fccb5-115">Example 1: Create an integration account map</span></span>
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

<span data-ttu-id="fccb5-116">Mit diesem Befehl wird die Integrationskontozuordnung in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="fccb5-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="fccb5-117">Der Befehl gibt eine Kartendefinition an, die in der $MapContent durch einen vorherigen Befehl gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="fccb5-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="fccb5-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fccb5-118">Example 2</span></span>

<span data-ttu-id="fccb5-119">Erstellt eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="fccb5-119">Creates an integration account map.</span></span> <span data-ttu-id="fccb5-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="fccb5-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="fccb5-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fccb5-121">PARAMETERS</span></span>

### <span data-ttu-id="fccb5-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="fccb5-122">-ContentType</span></span>
<span data-ttu-id="fccb5-123">Gibt einen Inhaltstyp für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="fccb5-124">Dieses Cmdlet unterstützt Application/xml als Karteninhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="fccb5-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="fccb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fccb5-125">-DefaultProfile</span></span>
<span data-ttu-id="fccb5-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fccb5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fccb5-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="fccb5-127">-MapDefinition</span></span>
<span data-ttu-id="fccb5-128">Gibt ein Definitionsobjekt für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="fccb5-129">Geben Sie entweder diesen Parameter oder den *Parameter MapFilePath* an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="fccb5-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="fccb5-130">-MapFilePath</span></span>
<span data-ttu-id="fccb5-131">Gibt den Dateipfad einer Definition für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="fccb5-132">Geben Sie entweder diesen Parameter oder den *Parameter MapDefinition* an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="fccb5-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="fccb5-133">-MapName</span></span>
<span data-ttu-id="fccb5-134">Gibt einen Namen für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="fccb5-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="fccb5-135">-MapType</span></span>
<span data-ttu-id="fccb5-136">Gibt den Typ für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="fccb5-137">Dieses Cmdlet unterstützt Xslt als Kartentyp.</span><span class="sxs-lookup"><span data-stu-id="fccb5-137">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="fccb5-138">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fccb5-138">-Metadata</span></span>
<span data-ttu-id="fccb5-139">Gibt ein Metadatenobjekt für die Karte an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="fccb5-140">-Name</span><span class="sxs-lookup"><span data-stu-id="fccb5-140">-Name</span></span>
<span data-ttu-id="fccb5-141">Gibt einen Namen für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="fccb5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fccb5-142">-ResourceGroupName</span></span>
<span data-ttu-id="fccb5-143">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fccb5-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fccb5-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fccb5-144">-Confirm</span></span>
<span data-ttu-id="fccb5-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fccb5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fccb5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fccb5-146">-WhatIf</span></span>
<span data-ttu-id="fccb5-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fccb5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fccb5-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fccb5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fccb5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fccb5-149">CommonParameters</span></span>
<span data-ttu-id="fccb5-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fccb5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fccb5-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fccb5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fccb5-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fccb5-152">INPUTS</span></span>

### <span data-ttu-id="fccb5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="fccb5-153">System.String</span></span>

## <span data-ttu-id="fccb5-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fccb5-154">OUTPUTS</span></span>

### <span data-ttu-id="fccb5-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="fccb5-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="fccb5-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fccb5-156">NOTES</span></span>

## <span data-ttu-id="fccb5-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fccb5-157">RELATED LINKS</span></span>

[<span data-ttu-id="fccb5-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="fccb5-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="fccb5-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="fccb5-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="fccb5-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="fccb5-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


