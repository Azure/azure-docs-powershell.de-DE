---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503905"
---
# <span data-ttu-id="721fc-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="721fc-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="721fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="721fc-102">SYNOPSIS</span></span>
<span data-ttu-id="721fc-103">Importiert ein Zertifikat in einem PFX-Format für einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="721fc-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="721fc-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="721fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="721fc-105">DESCRIPTION</span></span>
<span data-ttu-id="721fc-106">Mit dem Cmdlet " **Import-AzureRmApiManagementHostnameCertificate** " wird ein Zertifikat in einem PFX-Format für einen API-Verwaltungsdienst importiert.</span><span class="sxs-lookup"><span data-stu-id="721fc-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="721fc-107">Das Zertifikat ist für die Konfiguration von benutzerdefinierten Hostnamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="721fc-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="721fc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="721fc-108">EXAMPLES</span></span>

### <span data-ttu-id="721fc-109">Beispiel 1: Importieren eines Host-Zertifikats für die API-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="721fc-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="721fc-110">Mit diesem Befehl wird ein Zertifikat für einen benutzerdefinierten Proxy-Hostname importiert.</span><span class="sxs-lookup"><span data-stu-id="721fc-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="721fc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="721fc-111">PARAMETERS</span></span>

### <span data-ttu-id="721fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721fc-112">-DefaultProfile</span></span>
<span data-ttu-id="721fc-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="721fc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="721fc-114">-HostNameType</span><span class="sxs-lookup"><span data-stu-id="721fc-114">-HostnameType</span></span>
<span data-ttu-id="721fc-115">Gibt den Host Namenstyp an, für den dieses Cmdlet das Zertifikat lädt.</span><span class="sxs-lookup"><span data-stu-id="721fc-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="721fc-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="721fc-116">Valid values are:</span></span> 

- <span data-ttu-id="721fc-117">Proxy</span><span class="sxs-lookup"><span data-stu-id="721fc-117">Proxy</span></span>
- <span data-ttu-id="721fc-118">Portal</span><span class="sxs-lookup"><span data-stu-id="721fc-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721fc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="721fc-119">-Name</span></span>
<span data-ttu-id="721fc-120">Gibt den Namen der API-Verwaltungs Bereitstellung an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="721fc-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="721fc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721fc-121">-PassThru</span></span>
<span data-ttu-id="721fc-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="721fc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="721fc-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="721fc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="721fc-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="721fc-124">-PfxPassword</span></span>
<span data-ttu-id="721fc-125">Gibt das Kennwort für die PFX-Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="721fc-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721fc-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="721fc-126">-PfxPath</span></span>
<span data-ttu-id="721fc-127">Gibt den Pfad zu einer PFX-Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="721fc-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="721fc-129">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="721fc-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="721fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721fc-130">CommonParameters</span></span>
<span data-ttu-id="721fc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721fc-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721fc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="721fc-133">INPUTS</span></span>

### <span data-ttu-id="721fc-134">Keine</span><span class="sxs-lookup"><span data-stu-id="721fc-134">None</span></span>
<span data-ttu-id="721fc-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="721fc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="721fc-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="721fc-136">OUTPUTS</span></span>

### <span data-ttu-id="721fc-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="721fc-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="721fc-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="721fc-138">NOTES</span></span>

## <span data-ttu-id="721fc-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="721fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="721fc-140">Neu – AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="721fc-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="721fc-141">Satz-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="721fc-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


