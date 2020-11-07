---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: c8d3ff0d268c4a84269585af7e769b46af663f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658291"
---
# <span data-ttu-id="2bccd-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="2bccd-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="2bccd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bccd-102">SYNOPSIS</span></span>
<span data-ttu-id="2bccd-103">Ruft den Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="2bccd-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="2bccd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bccd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bccd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bccd-105">DESCRIPTION</span></span>
<span data-ttu-id="2bccd-106">Das Cmdlet " **Get-AzApiManagementTenantSyncState** " Ruft den Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository ab.</span><span class="sxs-lookup"><span data-stu-id="2bccd-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="2bccd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bccd-107">EXAMPLES</span></span>

### <span data-ttu-id="2bccd-108">Beispiel 1: Abrufen des Status der letzten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="2bccd-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="2bccd-109">Mit diesem Befehl wird der Status der letzten Synchronisierung zwischen der Konfigurationsdatenbank und dem git-Repository abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2bccd-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="2bccd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bccd-110">PARAMETERS</span></span>

### <span data-ttu-id="2bccd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2bccd-111">-Context</span></span>
<span data-ttu-id="2bccd-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2bccd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2bccd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bccd-113">-DefaultProfile</span></span>
<span data-ttu-id="2bccd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bccd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bccd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bccd-115">CommonParameters</span></span>
<span data-ttu-id="2bccd-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bccd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bccd-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bccd-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bccd-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bccd-118">INPUTS</span></span>

### <span data-ttu-id="2bccd-119">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2bccd-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="2bccd-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bccd-120">OUTPUTS</span></span>

### <span data-ttu-id="2bccd-121">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="2bccd-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="2bccd-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bccd-122">NOTES</span></span>

## <span data-ttu-id="2bccd-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bccd-123">RELATED LINKS</span></span>
