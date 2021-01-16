---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381658"
---
# <span data-ttu-id="2f2ca-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2f2ca-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="2f2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2ca-103">Legt die angegebene Bereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="2f2ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f2ca-104">SYNTAX</span></span>

### <span data-ttu-id="2f2ca-105">SetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f2ca-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f2ca-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="2f2ca-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f2ca-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="2f2ca-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f2ca-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="2f2ca-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f2ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f2ca-109">DESCRIPTION</span></span>
<span data-ttu-id="2f2ca-110">Das **Cmdlet "Set-AzApiManagementPolicy"** legt die angegebene Bereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="2f2ca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f2ca-111">EXAMPLES</span></span>

### <span data-ttu-id="2f2ca-112">Beispiel 1: Festlegen der Richtlinie auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="2f2ca-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="2f2ca-113">Mit diesem Befehl wird die Richtlinie auf Mandantenebene aus einer Datei namens "tenantpolicy.xml" tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="2f2ca-114">Beispiel 2: Festlegen einer Produktbereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2f2ca-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="2f2ca-115">Dieser Befehl legt die Produktbereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="2f2ca-116">Beispiel 3: Festlegen einer RICHTLINIE für den API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2f2ca-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="2f2ca-117">Mit diesem Befehl wird die API-Bereichsrichtlinie für die API-Verwaltung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="2f2ca-118">Beispiel 4: Festlegen einer Vorgangsbereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2f2ca-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="2f2ca-119">Dieser Befehl legt eine Vorgangsbereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="2f2ca-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f2ca-120">PARAMETERS</span></span>

### <span data-ttu-id="2f2ca-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f2ca-121">-ApiId</span></span>
<span data-ttu-id="2f2ca-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="2f2ca-123">Wenn Sie diesen Parameter angeben, legt das Cmdlet die Richtlinie für den API-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="2f2ca-124">-ApiRevision</span></span>
<span data-ttu-id="2f2ca-125">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-125">Identifier of API Revision.</span></span> <span data-ttu-id="2f2ca-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-126">This parameter is optional.</span></span> <span data-ttu-id="2f2ca-127">Wenn nichts angegeben wird, wird die Richtlinie in der derzeit aktiven API-Überarbeitung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-128">-Context</span><span class="sxs-lookup"><span data-stu-id="2f2ca-128">-Context</span></span>
<span data-ttu-id="2f2ca-129">Gibt die Instanz von **PsApiManagementContext an.**</span><span class="sxs-lookup"><span data-stu-id="2f2ca-129">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2ca-130">-DefaultProfile</span></span>
<span data-ttu-id="2f2ca-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f2ca-132">-Format</span><span class="sxs-lookup"><span data-stu-id="2f2ca-132">-Format</span></span>
<span data-ttu-id="2f2ca-133">Gibt das Format der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-133">Specifies the format of the policy.</span></span> <span data-ttu-id="2f2ca-134">Bei Verwendung müssen in der Richtlinie enthaltene `application/vnd.ms-azure-apim.policy+xml` Ausdrücke mit einem XML-Escape-Code definiert werden.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="2f2ca-135">Wenn sie `application/vnd.ms-azure-apim.policy.raw+xml` verwendet **wird, muss** für die Richtlinie kein XML-Escape-Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="2f2ca-136">Der Standardwert ist `application/vnd.ms-azure-apim.policy+xml` " .</span><span class="sxs-lookup"><span data-stu-id="2f2ca-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="2f2ca-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f2ca-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2f2ca-138">-OperationId</span></span>
<span data-ttu-id="2f2ca-139">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="2f2ca-140">Bei Angabe mit "ApiId" wird die Richtlinie für den Vorgangsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="2f2ca-141">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f2ca-142">-PassThru</span></span>
<span data-ttu-id="2f2ca-143">passthru</span><span class="sxs-lookup"><span data-stu-id="2f2ca-143">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="2f2ca-144">-Policy</span></span>
<span data-ttu-id="2f2ca-145">Gibt das Richtliniendokument als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="2f2ca-146">Dieser Parameter ist erforderlich, wenn *"- PolicyFilePath"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="2f2ca-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="2f2ca-147">-PolicyFilePath</span></span>
<span data-ttu-id="2f2ca-148">Gibt den Dateipfad des Richtliniendokuments an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="2f2ca-149">Dieser Parameter ist erforderlich, wenn der *Parameter "Policy"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="2f2ca-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="2f2ca-150">-PolicyUrl</span></span>
<span data-ttu-id="2f2ca-151">Die URL, unter der das Richtliniendokument gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="2f2ca-152">Dieser Parameter ist erforderlich, wenn "-Policy" oder "-PolicyFilePath" nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="2f2ca-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2f2ca-153">-ProductId</span></span>
<span data-ttu-id="2f2ca-154">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="2f2ca-155">Wenn dieser Parameter angegeben wird, legt das Cmdlet die Richtlinie für den Produktbereich fest.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2ca-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2ca-156">CommonParameters</span></span>
<span data-ttu-id="2f2ca-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2ca-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2ca-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f2ca-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2ca-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f2ca-159">INPUTS</span></span>

### <span data-ttu-id="2f2ca-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f2ca-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f2ca-161">System.String</span><span class="sxs-lookup"><span data-stu-id="2f2ca-161">System.String</span></span>

### <span data-ttu-id="2f2ca-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f2ca-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f2ca-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f2ca-163">OUTPUTS</span></span>

### <span data-ttu-id="2f2ca-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f2ca-164">System.Boolean</span></span>

## <span data-ttu-id="2f2ca-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f2ca-165">NOTES</span></span>

## <span data-ttu-id="2f2ca-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f2ca-166">RELATED LINKS</span></span>

[<span data-ttu-id="2f2ca-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2f2ca-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="2f2ca-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2f2ca-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


