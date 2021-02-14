---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176300"
---
# <span data-ttu-id="97cb0-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="97cb0-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="97cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="97cb0-103">Erstellt eine Instanz von "PsApiManagementSslSetting".</span><span class="sxs-lookup"><span data-stu-id="97cb0-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="97cb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97cb0-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97cb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="97cb0-106">Hilfsbefehl zum Erstellen einer Instanz von "PsApiManagementSslSetting".</span><span class="sxs-lookup"><span data-stu-id="97cb0-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="97cb0-107">Dieser Befehl wird zusammen mit dem Befehl New-AzApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="97cb0-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="97cb0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97cb0-108">EXAMPLES</span></span>

### <span data-ttu-id="97cb0-109">Beispiel 1: Erstellen einer SSL-Einstellung zum Aktivieren von TLS 1.0 für Back-End und Frontend</span><span class="sxs-lookup"><span data-stu-id="97cb0-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="97cb0-110">Erstellen Sie eine neue Instanz von PsApiManagementSslSetting, um TLSv 1.0 sowohl im Frontend (zwischen Client und APIM) als auch im Back-End (zwischen APIM und Back-End) des ApiManagement Gateways zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="97cb0-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="97cb0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97cb0-111">PARAMETERS</span></span>

### <span data-ttu-id="97cb0-112">-Back-EndProtocol</span><span class="sxs-lookup"><span data-stu-id="97cb0-112">-BackendProtocol</span></span>
<span data-ttu-id="97cb0-113">Back-End-Sicherheitsprotokolleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="97cb0-113">Backend Security protocol settings.</span></span> <span data-ttu-id="97cb0-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="97cb0-114">This parameter is optional.</span></span>
<span data-ttu-id="97cb0-115">Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="97cb0-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cb0-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="97cb0-116">-CipherSuite</span></span>
<span data-ttu-id="97cb0-117">Einstellungen der Ssl-Verschlüsselungssammlung in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="97cb0-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="97cb0-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="97cb0-118">This parameter is optional.</span></span>
<span data-ttu-id="97cb0-119">Die gültigen Einstellungen sind `TripleDes168` : "Tripe Des 168 aktivieren/deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="97cb0-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cb0-120">-DefaultProfile</span></span>
<span data-ttu-id="97cb0-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97cb0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97cb0-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="97cb0-122">-FrontendProtocol</span></span>
<span data-ttu-id="97cb0-123">Einstellungen für Frontend Security-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="97cb0-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="97cb0-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="97cb0-124">This parameter is optional.</span></span>
<span data-ttu-id="97cb0-125">Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="97cb0-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cb0-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="97cb0-126">-ServerProtocol</span></span>
<span data-ttu-id="97cb0-127">Serverprotokolleinstellungen wie Http2.</span><span class="sxs-lookup"><span data-stu-id="97cb0-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="97cb0-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="97cb0-128">This parameter is optional.</span></span>
<span data-ttu-id="97cb0-129">Die gültigen Einstellungen sind `Http2` – Http 2.0 aktivieren</span><span class="sxs-lookup"><span data-stu-id="97cb0-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97cb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cb0-130">CommonParameters</span></span>
<span data-ttu-id="97cb0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cb0-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97cb0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cb0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97cb0-133">INPUTS</span></span>

### <span data-ttu-id="97cb0-134">Keine</span><span class="sxs-lookup"><span data-stu-id="97cb0-134">None</span></span>

## <span data-ttu-id="97cb0-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97cb0-135">OUTPUTS</span></span>

### <span data-ttu-id="97cb0-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="97cb0-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="97cb0-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97cb0-137">NOTES</span></span>

## <span data-ttu-id="97cb0-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97cb0-138">RELATED LINKS</span></span>

[<span data-ttu-id="97cb0-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="97cb0-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

