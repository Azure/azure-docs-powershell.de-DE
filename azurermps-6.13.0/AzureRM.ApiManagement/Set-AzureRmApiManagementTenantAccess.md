---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c8f05c7ca9ddeb5868d62633600d63f5d7f01be0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478018"
---
# <span data-ttu-id="ab55e-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ab55e-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="ab55e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab55e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab55e-103">Aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ab55e-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab55e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab55e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab55e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab55e-105">DESCRIPTION</span></span>
<span data-ttu-id="ab55e-106">Das Cmdlet " **Satz-AzureRmApiManagementTenantAccess** " aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ab55e-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="ab55e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab55e-107">EXAMPLES</span></span>

### <span data-ttu-id="ab55e-108">Beispiel 1: Aktivieren des Mandanten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="ab55e-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="ab55e-109">Dieser Befehl ermöglicht Mandanten Zugriff im angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="ab55e-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="ab55e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab55e-110">PARAMETERS</span></span>

### <span data-ttu-id="ab55e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ab55e-111">-Context</span></span>
<span data-ttu-id="ab55e-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ab55e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab55e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab55e-113">-DefaultProfile</span></span>
<span data-ttu-id="ab55e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab55e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab55e-115">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ab55e-115">-Enabled</span></span>
<span data-ttu-id="ab55e-116">Gibt an, ob das Cmdlet den Mandanten Zugriff aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab55e-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="ab55e-117">Geben Sie einen Wert für $true an, den Sie aktivieren oder deaktivieren $false.</span><span class="sxs-lookup"><span data-stu-id="ab55e-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab55e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab55e-118">-PassThru</span></span>
<span data-ttu-id="ab55e-119">Gibt an, dass dieses Cmdlet die **PsApiManagementAccessInformation** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ab55e-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ab55e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab55e-120">CommonParameters</span></span>
<span data-ttu-id="ab55e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab55e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab55e-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab55e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab55e-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab55e-123">INPUTS</span></span>

### <span data-ttu-id="ab55e-124">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab55e-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab55e-125">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ab55e-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab55e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab55e-126">OUTPUTS</span></span>

### <span data-ttu-id="ab55e-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ab55e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ab55e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab55e-128">NOTES</span></span>

## <span data-ttu-id="ab55e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab55e-129">RELATED LINKS</span></span>

[<span data-ttu-id="ab55e-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ab55e-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


