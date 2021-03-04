---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932096"
---
# <span data-ttu-id="fe243-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="fe243-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="fe243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe243-102">SYNOPSIS</span></span>
<span data-ttu-id="fe243-103">Aktiviert oder deaktiviert den Mandantenzugriff.</span><span class="sxs-lookup"><span data-stu-id="fe243-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="fe243-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe243-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe243-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe243-105">DESCRIPTION</span></span>
<span data-ttu-id="fe243-106">Das **Cmdlet Set-AzApiManagementTenantAccess** aktiviert oder deaktiviert den Mandantenzugriff.</span><span class="sxs-lookup"><span data-stu-id="fe243-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="fe243-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe243-107">EXAMPLES</span></span>

### <span data-ttu-id="fe243-108">Beispiel 1: Aktivieren des Mandantenzugriffs</span><span class="sxs-lookup"><span data-stu-id="fe243-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="fe243-109">Dieser Befehl ermöglicht den Mandantenzugriff im angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="fe243-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="fe243-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fe243-110">PARAMETERS</span></span>

### <span data-ttu-id="fe243-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fe243-111">-Context</span></span>
<span data-ttu-id="fe243-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="fe243-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe243-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe243-113">-DefaultProfile</span></span>
<span data-ttu-id="fe243-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe243-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe243-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="fe243-115">-Enabled</span></span>
<span data-ttu-id="fe243-116">Gibt an, ob dieses Cmdlet den Mandantenzugriff aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fe243-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="fe243-117">Geben Sie einen Wert von $True an, um das $False zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fe243-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="fe243-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe243-118">-PassThru</span></span>
<span data-ttu-id="fe243-119">Gibt an, dass dieses Cmdlet die **PsApiManagementAccessInformation zurückgibt,** die dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="fe243-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fe243-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe243-120">CommonParameters</span></span>
<span data-ttu-id="fe243-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe243-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe243-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe243-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe243-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe243-123">INPUTS</span></span>

### <span data-ttu-id="fe243-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe243-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe243-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fe243-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe243-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe243-126">OUTPUTS</span></span>

### <span data-ttu-id="fe243-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="fe243-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="fe243-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fe243-128">NOTES</span></span>

## <span data-ttu-id="fe243-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fe243-129">RELATED LINKS</span></span>

[<span data-ttu-id="fe243-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="fe243-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


