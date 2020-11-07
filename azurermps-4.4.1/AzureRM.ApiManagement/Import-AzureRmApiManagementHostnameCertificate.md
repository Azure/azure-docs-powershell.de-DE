---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 5d931551491a0df67252f90f6052fdebde15492b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662984"
---
# <span data-ttu-id="06202-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="06202-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="06202-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06202-102">SYNOPSIS</span></span>
<span data-ttu-id="06202-103">Importiert ein Zertifikat in einem PFX-Format für einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="06202-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06202-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06202-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06202-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06202-105">DESCRIPTION</span></span>
<span data-ttu-id="06202-106">Mit dem Cmdlet " **Import-AzureRmApiManagementHostnameCertificate** " wird ein Zertifikat in einem PFX-Format für einen API-Verwaltungsdienst importiert.</span><span class="sxs-lookup"><span data-stu-id="06202-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="06202-107">Das Zertifikat ist für die Konfiguration von benutzerdefinierten Hostnamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="06202-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="06202-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06202-108">EXAMPLES</span></span>

### <span data-ttu-id="06202-109">Beispiel 1: Importieren eines Host-Zertifikats für die API-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="06202-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="06202-110">Mit diesem Befehl wird ein Zertifikat für einen benutzerdefinierten Proxy-Hostname importiert.</span><span class="sxs-lookup"><span data-stu-id="06202-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="06202-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="06202-111">PARAMETERS</span></span>

### <span data-ttu-id="06202-112">-HostNameType</span><span class="sxs-lookup"><span data-stu-id="06202-112">-HostnameType</span></span>
<span data-ttu-id="06202-113">Gibt den Host Namenstyp an, für den dieses Cmdlet das Zertifikat lädt.</span><span class="sxs-lookup"><span data-stu-id="06202-113">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="06202-114">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="06202-114">Valid values are:</span></span> 

- <span data-ttu-id="06202-115">Proxy</span><span class="sxs-lookup"><span data-stu-id="06202-115">Proxy</span></span>
- <span data-ttu-id="06202-116">Portal</span><span class="sxs-lookup"><span data-stu-id="06202-116">Portal</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06202-117">-Name</span><span class="sxs-lookup"><span data-stu-id="06202-117">-Name</span></span>
<span data-ttu-id="06202-118">Gibt den Namen der API-Verwaltungs Bereitstellung an, die dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="06202-118">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="06202-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06202-119">-PassThru</span></span>
<span data-ttu-id="06202-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="06202-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06202-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="06202-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06202-122">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="06202-122">-PfxPassword</span></span>
<span data-ttu-id="06202-123">Gibt das Kennwort für die PFX-Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="06202-123">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06202-124">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="06202-124">-PfxPath</span></span>
<span data-ttu-id="06202-125">Gibt den Pfad zu einer PFX-Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="06202-125">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06202-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06202-126">-ResourceGroupName</span></span>
<span data-ttu-id="06202-127">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="06202-127">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="06202-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06202-128">-DefaultProfile</span></span>
<span data-ttu-id="06202-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06202-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06202-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06202-130">CommonParameters</span></span>
<span data-ttu-id="06202-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06202-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06202-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06202-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06202-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06202-133">INPUTS</span></span>

## <span data-ttu-id="06202-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06202-134">OUTPUTS</span></span>

### <span data-ttu-id="06202-135">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="06202-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="06202-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="06202-136">NOTES</span></span>

## <span data-ttu-id="06202-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06202-137">RELATED LINKS</span></span>

[<span data-ttu-id="06202-138">Neu – AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="06202-138">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="06202-139">Satz-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="06202-139">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


