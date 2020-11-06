---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502450"
---
# <span data-ttu-id="23607-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23607-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="23607-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23607-102">SYNOPSIS</span></span>
<span data-ttu-id="23607-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="23607-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23607-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23607-104">SYNTAX</span></span>

### <span data-ttu-id="23607-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="23607-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="23607-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="23607-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="23607-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="23607-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="23607-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="23607-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23607-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="23607-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23607-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23607-113">DESCRIPTION</span></span>
<span data-ttu-id="23607-114">Das Cmdlet **Test-AzureRmResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="23607-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="23607-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23607-115">EXAMPLES</span></span>

## <span data-ttu-id="23607-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="23607-116">PARAMETERS</span></span>

### <span data-ttu-id="23607-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23607-117">-ApiVersion</span></span>
<span data-ttu-id="23607-118">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="23607-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="23607-119">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="23607-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="23607-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23607-120">-DefaultProfile</span></span>
<span data-ttu-id="23607-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="23607-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23607-122">-Modus</span><span class="sxs-lookup"><span data-stu-id="23607-122">-Mode</span></span>
<span data-ttu-id="23607-123">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="23607-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="23607-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="23607-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23607-125">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="23607-125">Incremental</span></span>
- <span data-ttu-id="23607-126">Komplette</span><span class="sxs-lookup"><span data-stu-id="23607-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="23607-127">-Pre</span></span>
<span data-ttu-id="23607-128">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="23607-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23607-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23607-129">-ResourceGroupName</span></span>
<span data-ttu-id="23607-130">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="23607-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="23607-131">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="23607-131">-TemplateFile</span></span>
<span data-ttu-id="23607-132">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="23607-132">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="23607-133">-TemplateParameterFile</span></span>
<span data-ttu-id="23607-134">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="23607-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="23607-135">-TemplateParameterObject</span></span>
<span data-ttu-id="23607-136">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="23607-136">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="23607-137">-TemplateParameterUri</span></span>
<span data-ttu-id="23607-138">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="23607-138">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="23607-139">-TemplateUri</span></span>
<span data-ttu-id="23607-140">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="23607-140">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23607-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23607-141">CommonParameters</span></span>
<span data-ttu-id="23607-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23607-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23607-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23607-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23607-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23607-144">INPUTS</span></span>

### <span data-ttu-id="23607-145">Keine</span><span class="sxs-lookup"><span data-stu-id="23607-145">None</span></span>
<span data-ttu-id="23607-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="23607-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23607-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23607-147">OUTPUTS</span></span>

### <span data-ttu-id="23607-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="23607-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="23607-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="23607-149">NOTES</span></span>

## <span data-ttu-id="23607-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23607-150">RELATED LINKS</span></span>

[<span data-ttu-id="23607-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23607-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23607-152">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23607-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23607-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23607-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23607-154">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23607-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


