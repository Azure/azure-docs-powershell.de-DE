---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477398"
---
# <span data-ttu-id="721cc-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="721cc-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="721cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="721cc-102">SYNOPSIS</span></span>
<span data-ttu-id="721cc-103">Aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="721cc-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="721cc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="721cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="721cc-105">DESCRIPTION</span></span>
<span data-ttu-id="721cc-106">Das Cmdlet " **Satz-AzureRmApiManagementTenantAccess** " aktiviert oder deaktiviert den Mandanten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="721cc-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="721cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="721cc-107">EXAMPLES</span></span>

### <span data-ttu-id="721cc-108">Beispiel 1: Aktivieren des Mandanten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="721cc-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="721cc-109">Dieser Befehl ermöglicht Mandanten Zugriff im angegebenen Kontext.</span><span class="sxs-lookup"><span data-stu-id="721cc-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="721cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="721cc-110">PARAMETERS</span></span>

### <span data-ttu-id="721cc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="721cc-111">-Context</span></span>
<span data-ttu-id="721cc-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="721cc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="721cc-113">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="721cc-113">-Enabled</span></span>
<span data-ttu-id="721cc-114">Gibt an, ob das Cmdlet den Mandanten Zugriff aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="721cc-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="721cc-115">Geben Sie einen Wert für $true an, den Sie aktivieren oder deaktivieren $false.</span><span class="sxs-lookup"><span data-stu-id="721cc-115">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="721cc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721cc-116">-PassThru</span></span>
<span data-ttu-id="721cc-117">Gibt an, dass dieses Cmdlet die **PsApiManagementAccessInformation** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="721cc-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="721cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721cc-118">-DefaultProfile</span></span>
<span data-ttu-id="721cc-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="721cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721cc-120">CommonParameters</span></span>
<span data-ttu-id="721cc-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721cc-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721cc-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="721cc-123">INPUTS</span></span>

## <span data-ttu-id="721cc-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="721cc-124">OUTPUTS</span></span>

### <span data-ttu-id="721cc-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="721cc-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="721cc-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="721cc-126">NOTES</span></span>

## <span data-ttu-id="721cc-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="721cc-127">RELATED LINKS</span></span>

[<span data-ttu-id="721cc-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="721cc-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


