---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478041"
---
# <span data-ttu-id="244d7-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="244d7-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="244d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="244d7-102">SYNOPSIS</span></span>
<span data-ttu-id="244d7-103">Legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="244d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="244d7-104">SYNTAX</span></span>

### <span data-ttu-id="244d7-105">SetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="244d7-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="244d7-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="244d7-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="244d7-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="244d7-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="244d7-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="244d7-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="244d7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="244d7-109">DESCRIPTION</span></span>
<span data-ttu-id="244d7-110">Das Cmdlet " **Set-AzureRmApiManagementPolicy** " legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="244d7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="244d7-111">EXAMPLES</span></span>

### <span data-ttu-id="244d7-112">Beispiel 1: Festlegen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="244d7-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="244d7-113">Dieser Befehl legt die Richtlinie für Mandantenebene aus einer Datei mit dem Namen tenantpolicy.xml fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="244d7-114">Beispiel 2: Festlegen einer Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="244d7-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="244d7-115">Dieser Befehl legt die Richtlinie für den Produktbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="244d7-116">Beispiel 3: Festlegen von API-Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="244d7-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="244d7-117">Dieser Befehl legt API-Bereichs Richtlinien für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="244d7-118">Beispiel 4: Festlegen des Vorgangs Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="244d7-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="244d7-119">Dieser Befehl legt die Richtlinie für den Vorgangsbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="244d7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="244d7-120">PARAMETERS</span></span>

### <span data-ttu-id="244d7-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="244d7-121">-ApiId</span></span>
<span data-ttu-id="244d7-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="244d7-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="244d7-123">Wenn Sie diesen Parameter angeben, legt das Cmdlet die Richtlinie für den API-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="244d7-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="244d7-124">-ApiRevision</span></span>
<span data-ttu-id="244d7-125">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="244d7-125">Identifier of API Revision.</span></span> <span data-ttu-id="244d7-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="244d7-126">This parameter is optional.</span></span> <span data-ttu-id="244d7-127">Wenn Sie nicht angegeben wird, wird die Richtlinie in der aktuell aktiven API-Revision aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="244d7-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="244d7-128">-Context</span><span class="sxs-lookup"><span data-stu-id="244d7-128">-Context</span></span>
<span data-ttu-id="244d7-129">Gibt die Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="244d7-129">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="244d7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244d7-130">-DefaultProfile</span></span>
<span data-ttu-id="244d7-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="244d7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="244d7-132">-Format</span><span class="sxs-lookup"><span data-stu-id="244d7-132">-Format</span></span>
<span data-ttu-id="244d7-133">Gibt das Format der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="244d7-133">Specifies the format of the policy.</span></span> <span data-ttu-id="244d7-134">Bei `application/vnd.ms-azure-apim.policy+xml` der Verwendung müssen Ausdrücke, die in der Richtlinie enthalten sind, mit XML-Escapezeichen versehen sein.</span><span class="sxs-lookup"><span data-stu-id="244d7-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="244d7-135">Bei Verwendung `application/vnd.ms-azure-apim.policy.raw+xml` ist es **nicht** erforderlich, dass die Richtlinie XML-escaped ist.</span><span class="sxs-lookup"><span data-stu-id="244d7-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="244d7-136">Der Standardwert ist `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="244d7-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="244d7-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="244d7-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="244d7-138">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="244d7-138">-OperationId</span></span>
<span data-ttu-id="244d7-139">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="244d7-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="244d7-140">Wenn mit ApiId angegeben, wird die Richtlinie für den Vorgangsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="244d7-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="244d7-141">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="244d7-141">This parameters is required.</span></span>

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

### <span data-ttu-id="244d7-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="244d7-142">-PassThru</span></span>
<span data-ttu-id="244d7-143">passthru</span><span class="sxs-lookup"><span data-stu-id="244d7-143">passthru</span></span>

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

### <span data-ttu-id="244d7-144">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="244d7-144">-Policy</span></span>
<span data-ttu-id="244d7-145">Gibt das Richtliniendokument als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="244d7-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="244d7-146">Dieser Parameter ist erforderlich, wenn die- *PolicyFilePath* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="244d7-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="244d7-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="244d7-147">-PolicyFilePath</span></span>
<span data-ttu-id="244d7-148">Gibt den Pfad der Richtliniendokument Datei an.</span><span class="sxs-lookup"><span data-stu-id="244d7-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="244d7-149">Dieser Parameter ist erforderlich, wenn der *Richtlinien* Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="244d7-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="244d7-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="244d7-150">-PolicyUrl</span></span>
<span data-ttu-id="244d7-151">Die URL, in der das Richtliniendokument gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="244d7-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="244d7-152">Dieser Parameter ist erforderlich, wenn-Policy oder-PolicyFilePath nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="244d7-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="244d7-153">-ProductID</span><span class="sxs-lookup"><span data-stu-id="244d7-153">-ProductId</span></span>
<span data-ttu-id="244d7-154">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="244d7-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="244d7-155">Wenn dieser Parameter angegeben wird, legt das Cmdlet die Richtlinie für den Produktbereich fest.</span><span class="sxs-lookup"><span data-stu-id="244d7-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="244d7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244d7-156">CommonParameters</span></span>
<span data-ttu-id="244d7-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="244d7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244d7-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="244d7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244d7-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="244d7-159">INPUTS</span></span>

### <span data-ttu-id="244d7-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="244d7-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="244d7-161">System. String</span><span class="sxs-lookup"><span data-stu-id="244d7-161">System.String</span></span>

### <span data-ttu-id="244d7-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="244d7-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="244d7-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="244d7-163">OUTPUTS</span></span>

### <span data-ttu-id="244d7-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="244d7-164">System.Boolean</span></span>

## <span data-ttu-id="244d7-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="244d7-165">NOTES</span></span>

## <span data-ttu-id="244d7-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="244d7-166">RELATED LINKS</span></span>

[<span data-ttu-id="244d7-167">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="244d7-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="244d7-168">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="244d7-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


