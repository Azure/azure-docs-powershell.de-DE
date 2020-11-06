---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: b9d7426bf275571d025ec0fef3f8bbec7c119c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503306"
---
# <span data-ttu-id="7c988-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="7c988-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="7c988-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c988-102">SYNOPSIS</span></span>
<span data-ttu-id="7c988-103">Ruft den Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="7c988-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c988-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c988-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c988-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c988-105">DESCRIPTION</span></span>
<span data-ttu-id="7c988-106">Das Cmdlet " **Get-AzureRmApiManagementTenantSyncState** " Ruft den Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="7c988-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="7c988-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c988-107">EXAMPLES</span></span>

### <span data-ttu-id="7c988-108">Beispiel 1: Abrufen des Status der letzten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="7c988-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $ApimContext
```

<span data-ttu-id="7c988-109">Mit diesem Befehl wird der Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c988-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="7c988-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c988-110">PARAMETERS</span></span>

### <span data-ttu-id="7c988-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7c988-111">-Context</span></span>
<span data-ttu-id="7c988-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7c988-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7c988-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c988-113">-DefaultProfile</span></span>
<span data-ttu-id="7c988-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c988-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c988-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c988-115">CommonParameters</span></span>
<span data-ttu-id="7c988-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c988-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c988-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c988-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c988-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c988-118">INPUTS</span></span>

## <span data-ttu-id="7c988-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c988-119">OUTPUTS</span></span>

### <span data-ttu-id="7c988-120">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="7c988-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7c988-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c988-121">NOTES</span></span>

## <span data-ttu-id="7c988-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c988-122">RELATED LINKS</span></span>

