---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381617"
---
# <span data-ttu-id="ac258-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ac258-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="ac258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac258-102">SYNOPSIS</span></span>
<span data-ttu-id="ac258-103">Aktiviert oder deaktiviert den Mandantenzugriff.</span><span class="sxs-lookup"><span data-stu-id="ac258-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="ac258-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac258-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac258-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac258-105">DESCRIPTION</span></span>
<span data-ttu-id="ac258-106">Das **Cmdlet "Set-AzApiManagementTenantAccess"** aktiviert oder deaktiviert den Mandantenzugriff.</span><span class="sxs-lookup"><span data-stu-id="ac258-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="ac258-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac258-107">EXAMPLES</span></span>

### <span data-ttu-id="ac258-108">Beispiel 1: Mandantenzugriff aktivieren</span><span class="sxs-lookup"><span data-stu-id="ac258-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="ac258-109">Dieser Befehl ermöglicht den Mandantenzugriff im angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="ac258-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="ac258-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac258-110">PARAMETERS</span></span>

### <span data-ttu-id="ac258-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ac258-111">-Context</span></span>
<span data-ttu-id="ac258-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ac258-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ac258-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac258-113">-DefaultProfile</span></span>
<span data-ttu-id="ac258-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac258-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac258-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ac258-115">-Enabled</span></span>
<span data-ttu-id="ac258-116">Gibt an, ob dieses Cmdlet den Mandantenzugriff aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac258-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="ac258-117">Geben Sie einen Wert für $True, den Sie aktivieren oder $False deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ac258-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="ac258-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac258-118">-PassThru</span></span>
<span data-ttu-id="ac258-119">Gibt an, dass dieses Cmdlet das von diesem Cmdlet geänderte **"PsApiManagementAccessInformation"** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ac258-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ac258-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac258-120">CommonParameters</span></span>
<span data-ttu-id="ac258-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac258-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac258-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac258-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac258-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac258-123">INPUTS</span></span>

### <span data-ttu-id="ac258-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac258-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac258-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac258-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac258-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac258-126">OUTPUTS</span></span>

### <span data-ttu-id="ac258-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="ac258-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="ac258-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac258-128">NOTES</span></span>

## <span data-ttu-id="ac258-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac258-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac258-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="ac258-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


