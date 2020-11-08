---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004373"
---
# <span data-ttu-id="b6c86-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b6c86-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="b6c86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6c86-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c86-103">Aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="b6c86-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="b6c86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6c86-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6c86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6c86-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c86-106">Das Cmdlet " **Satz-AzApiManagementTenantAccess** " aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="b6c86-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="b6c86-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6c86-107">EXAMPLES</span></span>

### <span data-ttu-id="b6c86-108">Beispiel 1: Aktivieren des Mandanten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="b6c86-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="b6c86-109">Dieser Befehl ermöglicht Mandanten Zugriff im angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="b6c86-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="b6c86-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6c86-110">PARAMETERS</span></span>

### <span data-ttu-id="b6c86-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b6c86-111">-Context</span></span>
<span data-ttu-id="b6c86-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6c86-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6c86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c86-113">-DefaultProfile</span></span>
<span data-ttu-id="b6c86-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6c86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6c86-115">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b6c86-115">-Enabled</span></span>
<span data-ttu-id="b6c86-116">Gibt an, ob das Cmdlet den Mandanten Zugriff aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b6c86-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="b6c86-117">Geben Sie einen Wert für $true an, den Sie aktivieren oder deaktivieren $false.</span><span class="sxs-lookup"><span data-stu-id="b6c86-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="b6c86-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6c86-118">-PassThru</span></span>
<span data-ttu-id="b6c86-119">Gibt an, dass dieses Cmdlet die **PsApiManagementAccessInformation** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b6c86-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6c86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c86-120">CommonParameters</span></span>
<span data-ttu-id="b6c86-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c86-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6c86-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c86-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6c86-123">INPUTS</span></span>

### <span data-ttu-id="b6c86-124">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6c86-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b6c86-125">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b6c86-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6c86-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6c86-126">OUTPUTS</span></span>

### <span data-ttu-id="b6c86-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b6c86-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b6c86-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6c86-128">NOTES</span></span>

## <span data-ttu-id="b6c86-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6c86-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6c86-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="b6c86-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


