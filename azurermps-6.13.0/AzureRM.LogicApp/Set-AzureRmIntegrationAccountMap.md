---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 331f2d4c7bba584f5989cd724a3e25abaedfa5c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664574"
---
# <span data-ttu-id="9ba82-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9ba82-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="9ba82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ba82-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba82-103">Ändert eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="9ba82-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba82-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ba82-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba82-106">Das Cmdlet " **Satz-AzureRmIntegrationAccountMap** " ändert eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="9ba82-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="9ba82-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontozuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ba82-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="9ba82-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="9ba82-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ba82-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9ba82-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="9ba82-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9ba82-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9ba82-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9ba82-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9ba82-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9ba82-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ba82-113">EXAMPLES</span></span>

### <span data-ttu-id="9ba82-114">Beispiel 1: Ändern einer Integration-Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="9ba82-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="9ba82-115">Mit diesem Befehl wird die Integrations Kontozuordnung in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="9ba82-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="9ba82-116">Der Befehl gibt eine Kartendefinition an, die von einem vorherigen Befehl in der $MapContent Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="9ba82-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="9ba82-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ba82-117">PARAMETERS</span></span>

### <span data-ttu-id="9ba82-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="9ba82-118">-ContentType</span></span>
<span data-ttu-id="9ba82-119">Gibt einen Inhaltstyp für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="9ba82-120">Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="9ba82-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="9ba82-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba82-121">-DefaultProfile</span></span>
<span data-ttu-id="9ba82-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ba82-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ba82-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9ba82-123">-Force</span></span>
<span data-ttu-id="9ba82-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9ba82-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ba82-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="9ba82-125">-MapDefinition</span></span>
<span data-ttu-id="9ba82-126">Gibt ein Definitionsobjekt für die Integration-Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="9ba82-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="9ba82-127">-MapFilePath</span></span>
<span data-ttu-id="9ba82-128">Gibt den Dateipfad einer Definition für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="9ba82-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="9ba82-129">-MapName</span></span>
<span data-ttu-id="9ba82-130">Gibt den Namen einer Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="9ba82-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="9ba82-131">-MapType</span></span>
<span data-ttu-id="9ba82-132">Gibt den Typ für die Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="9ba82-133">Dieses Cmdlet unterstützt XSLT als Kartentyp.</span><span class="sxs-lookup"><span data-stu-id="9ba82-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba82-134">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="9ba82-134">-Metadata</span></span>
<span data-ttu-id="9ba82-135">Gibt ein Metadatenobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="9ba82-136">-Name</span><span class="sxs-lookup"><span data-stu-id="9ba82-136">-Name</span></span>
<span data-ttu-id="9ba82-137">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9ba82-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba82-138">-ResourceGroupName</span></span>
<span data-ttu-id="9ba82-139">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9ba82-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9ba82-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ba82-140">-Confirm</span></span>
<span data-ttu-id="9ba82-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ba82-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba82-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba82-142">-WhatIf</span></span>
<span data-ttu-id="9ba82-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba82-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba82-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ba82-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba82-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba82-145">CommonParameters</span></span>
<span data-ttu-id="9ba82-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba82-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba82-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba82-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba82-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ba82-148">INPUTS</span></span>

### <span data-ttu-id="9ba82-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9ba82-149">System.String</span></span>

## <span data-ttu-id="9ba82-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ba82-150">OUTPUTS</span></span>

### <span data-ttu-id="9ba82-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9ba82-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="9ba82-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ba82-152">NOTES</span></span>

## <span data-ttu-id="9ba82-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ba82-153">RELATED LINKS</span></span>

[<span data-ttu-id="9ba82-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9ba82-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="9ba82-155">Neu – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9ba82-155">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="9ba82-156">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="9ba82-156">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


