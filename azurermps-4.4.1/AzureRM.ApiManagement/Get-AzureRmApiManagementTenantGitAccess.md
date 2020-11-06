---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503310"
---
# <span data-ttu-id="07061-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="07061-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="07061-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07061-102">SYNOPSIS</span></span>
<span data-ttu-id="07061-103">Ruft die git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="07061-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07061-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07061-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07061-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07061-105">DESCRIPTION</span></span>
<span data-ttu-id="07061-106">Das Cmdlet " **Get-AzureRmApiManagementTenantGitAccess** " Ruft die git-Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="07061-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="07061-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07061-107">EXAMPLES</span></span>

### <span data-ttu-id="07061-108">Beispiel 1: Abrufen der Mandanten Zugriffskonfiguration</span><span class="sxs-lookup"><span data-stu-id="07061-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="07061-109">Dieser Befehl ruft die git-Zugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="07061-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="07061-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07061-110">PARAMETERS</span></span>

### <span data-ttu-id="07061-111">-Context</span><span class="sxs-lookup"><span data-stu-id="07061-111">-Context</span></span>
<span data-ttu-id="07061-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="07061-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="07061-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07061-113">-DefaultProfile</span></span>
<span data-ttu-id="07061-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07061-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07061-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07061-115">CommonParameters</span></span>
<span data-ttu-id="07061-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07061-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07061-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07061-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07061-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07061-118">INPUTS</span></span>

## <span data-ttu-id="07061-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07061-119">OUTPUTS</span></span>

### <span data-ttu-id="07061-120">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="07061-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="07061-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="07061-121">NOTES</span></span>

## <span data-ttu-id="07061-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07061-122">RELATED LINKS</span></span>

