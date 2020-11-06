---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: defd5c046427115e44783d6b34ea7b034edc8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478057"
---
# <span data-ttu-id="ceb8a-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceb8a-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="ceb8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ceb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb8a-103">Erstellt eine Instanz von PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceb8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceb8a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ceb8a-105">DESCRIPTION</span></span>
<span data-ttu-id="ceb8a-106">Das Cmdlet **New-AzureRmApiManagementHostnameConfiguration** ist ein Hilfsbefehl, mit dem eine Instanz von **PsApiManagementHostnameConfiguration** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="ceb8a-107">Dieser Befehl wird mit dem Set-AzureRmApiManagementHostnames-Cmdlet verwendet.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="ceb8a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ceb8a-108">EXAMPLES</span></span>

### <span data-ttu-id="ceb8a-109">Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceb8a-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="ceb8a-110">Dieser Befehl erstellt und Initialisiert eine Instanz von **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="ceb8a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceb8a-111">PARAMETERS</span></span>

### <span data-ttu-id="ceb8a-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ceb8a-112">-CertificateThumbprint</span></span>
<span data-ttu-id="ceb8a-113">Gibt den Fingerabdruck des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="ceb8a-114">Das Zertifikat muss zuerst mit dem Import-AzureRmApiManagementHostnameCertificate-Cmdlet importiert werden.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

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

### <span data-ttu-id="ceb8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb8a-115">-DefaultProfile</span></span>
<span data-ttu-id="ceb8a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceb8a-117">-Hostname</span><span class="sxs-lookup"><span data-stu-id="ceb8a-117">-Hostname</span></span>
<span data-ttu-id="ceb8a-118">Gibt den benutzerdefinierten Host Namen an, für den dieses Cmdlet die **PsApiManagementHostnameConfiguration** -Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-118">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

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

### <span data-ttu-id="ceb8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb8a-119">CommonParameters</span></span>
<span data-ttu-id="ceb8a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb8a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb8a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb8a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ceb8a-122">INPUTS</span></span>

### <span data-ttu-id="ceb8a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ceb8a-123">None</span></span>

## <span data-ttu-id="ceb8a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ceb8a-124">OUTPUTS</span></span>

### <span data-ttu-id="ceb8a-125">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceb8a-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="ceb8a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ceb8a-126">NOTES</span></span>

## <span data-ttu-id="ceb8a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ceb8a-127">RELATED LINKS</span></span>

[<span data-ttu-id="ceb8a-128">Importieren-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ceb8a-128">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="ceb8a-129">Satz-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ceb8a-129">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


