---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662866"
---
# <span data-ttu-id="fdf07-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf07-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="fdf07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdf07-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf07-103">Legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf07-104">SYNTAX</span></span>

### <span data-ttu-id="fdf07-105">SetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="fdf07-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf07-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="fdf07-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf07-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="fdf07-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf07-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="fdf07-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf07-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdf07-109">DESCRIPTION</span></span>
<span data-ttu-id="fdf07-110">Das Cmdlet " **Set-AzureRmApiManagementPolicy** " legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="fdf07-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdf07-111">EXAMPLES</span></span>

### <span data-ttu-id="fdf07-112">Beispiel 1: Festlegen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="fdf07-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="fdf07-113">Dieser Befehl legt die Richtlinie für Mandantenebene aus einer Datei mit dem Namen tenantpolicy.xml fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="fdf07-114">Beispiel 2: Festlegen einer Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="fdf07-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="fdf07-115">Dieser Befehl legt die Richtlinie für den Produktbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="fdf07-116">Beispiel 3: Festlegen von API-Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fdf07-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="fdf07-117">Dieser Befehl legt API-Bereichs Richtlinien für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="fdf07-118">Beispiel 4: Festlegen des Vorgangs Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fdf07-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="fdf07-119">Dieser Befehl legt die Richtlinie für den Vorgangsbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="fdf07-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf07-120">PARAMETERS</span></span>

### <span data-ttu-id="fdf07-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fdf07-121">-ApiId</span></span>
<span data-ttu-id="fdf07-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="fdf07-123">Wenn Sie diesen Parameter angeben, legt das Cmdlet die Richtlinie für den API-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-124">-Context</span><span class="sxs-lookup"><span data-stu-id="fdf07-124">-Context</span></span>
<span data-ttu-id="fdf07-125">Gibt die Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-125">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf07-126">-DefaultProfile</span></span>
<span data-ttu-id="fdf07-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdf07-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fdf07-128">-Format</span><span class="sxs-lookup"><span data-stu-id="fdf07-128">-Format</span></span>
<span data-ttu-id="fdf07-129">Gibt das Format der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="fdf07-130">Der Standardwert ist "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="fdf07-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-131">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="fdf07-131">-OperationId</span></span>
<span data-ttu-id="fdf07-132">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="fdf07-133">Wenn mit ApiId angegeben, wird die Richtlinie für den Vorgangsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fdf07-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="fdf07-134">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fdf07-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf07-135">-PassThru</span></span>
<span data-ttu-id="fdf07-136">passthru</span><span class="sxs-lookup"><span data-stu-id="fdf07-136">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-137">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fdf07-137">-Policy</span></span>
<span data-ttu-id="fdf07-138">Gibt das Richtliniendokument als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="fdf07-139">Dieser Parameter ist erforderlich, wenn die- *PolicyFilePath* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fdf07-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="fdf07-140">-PolicyFilePath</span></span>
<span data-ttu-id="fdf07-141">Gibt den Pfad der Richtliniendokument Datei an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="fdf07-142">Dieser Parameter ist erforderlich, wenn der *Richtlinien* Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fdf07-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-143">-ProductID</span><span class="sxs-lookup"><span data-stu-id="fdf07-143">-ProductId</span></span>
<span data-ttu-id="fdf07-144">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="fdf07-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="fdf07-145">Wenn dieser Parameter angegeben wird, legt das Cmdlet die Richtlinie für den Produktbereich fest.</span><span class="sxs-lookup"><span data-stu-id="fdf07-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf07-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf07-146">CommonParameters</span></span>
<span data-ttu-id="fdf07-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf07-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf07-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf07-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf07-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdf07-149">INPUTS</span></span>

### <span data-ttu-id="fdf07-150">Keine</span><span class="sxs-lookup"><span data-stu-id="fdf07-150">None</span></span>
<span data-ttu-id="fdf07-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fdf07-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdf07-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdf07-152">OUTPUTS</span></span>

### <span data-ttu-id="fdf07-153">bool</span><span class="sxs-lookup"><span data-stu-id="fdf07-153">bool</span></span>

## <span data-ttu-id="fdf07-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdf07-154">NOTES</span></span>

## <span data-ttu-id="fdf07-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdf07-155">RELATED LINKS</span></span>

[<span data-ttu-id="fdf07-156">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf07-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="fdf07-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf07-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


