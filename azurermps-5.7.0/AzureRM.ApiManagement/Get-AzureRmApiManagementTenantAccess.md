---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 64f341398ff20f3eddf67c88c51a93125904d566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483214"
---
# <span data-ttu-id="8d1b7-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8d1b7-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="8d1b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1b7-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d1b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d1b7-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="8d1b7-106">Das Cmdlet " **Get-AzureRmApiManagementTenantAccess** " Ruft die Mandanten Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="8d1b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d1b7-107">EXAMPLES</span></span>

### <span data-ttu-id="8d1b7-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1b7-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext 
```

<span data-ttu-id="8d1b7-109">Dieser Befehl ruft die Mandanten Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="8d1b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d1b7-110">PARAMETERS</span></span>

### <span data-ttu-id="8d1b7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8d1b7-111">-Context</span></span>
<span data-ttu-id="8d1b7-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8d1b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1b7-113">-DefaultProfile</span></span>
<span data-ttu-id="8d1b7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8d1b7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1b7-115">CommonParameters</span></span>
<span data-ttu-id="8d1b7-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1b7-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1b7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1b7-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d1b7-118">INPUTS</span></span>

### <span data-ttu-id="8d1b7-119">Keine</span><span class="sxs-lookup"><span data-stu-id="8d1b7-119">None</span></span>
<span data-ttu-id="8d1b7-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8d1b7-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d1b7-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d1b7-121">OUTPUTS</span></span>

### <span data-ttu-id="8d1b7-122">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="8d1b7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="8d1b7-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d1b7-123">NOTES</span></span>

## <span data-ttu-id="8d1b7-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d1b7-124">RELATED LINKS</span></span>

[<span data-ttu-id="8d1b7-125">Satz-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8d1b7-125">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


