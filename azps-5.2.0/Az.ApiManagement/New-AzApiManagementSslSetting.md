---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308464"
---
# <span data-ttu-id="90420-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="90420-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="90420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90420-102">SYNOPSIS</span></span>
<span data-ttu-id="90420-103">Erstellt eine Instanz von "PsApiManagementSslSetting".</span><span class="sxs-lookup"><span data-stu-id="90420-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="90420-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90420-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90420-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90420-105">DESCRIPTION</span></span>
<span data-ttu-id="90420-106">Hilfsbefehl zum Erstellen einer Instanz von "PsApiManagementSslSetting".</span><span class="sxs-lookup"><span data-stu-id="90420-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="90420-107">Dieser Befehl wird zusammen mit dem Befehl New-AzApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="90420-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="90420-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90420-108">EXAMPLES</span></span>

### <span data-ttu-id="90420-109">Beispiel 1: Erstellen einer SSL-Einstellung zum Aktivieren von TLS 1.0 für Back-End und Frontend</span><span class="sxs-lookup"><span data-stu-id="90420-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="90420-110">Erstellen Sie eine neue Instanz von PsApiManagementSslSetting, um TLSv 1.0 sowohl im Frontend (zwischen Client und APIM) als auch im Back-End (zwischen APIM und Back-End) des ApiManagement Gateways zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="90420-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="90420-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90420-111">PARAMETERS</span></span>

### <span data-ttu-id="90420-112">-Back-EndProtocol</span><span class="sxs-lookup"><span data-stu-id="90420-112">-BackendProtocol</span></span>
<span data-ttu-id="90420-113">Back-End-Sicherheitsprotokolleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="90420-113">Backend Security protocol settings.</span></span> <span data-ttu-id="90420-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="90420-114">This parameter is optional.</span></span>
<span data-ttu-id="90420-115">Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="90420-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="90420-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="90420-116">-CipherSuite</span></span>
<span data-ttu-id="90420-117">Einstellungen der Ssl-Verschlüsselungssammlung in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="90420-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="90420-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="90420-118">This parameter is optional.</span></span>
<span data-ttu-id="90420-119">Die gültigen Einstellungen sind `TripleDes168` : "Tripe Des 168 aktivieren/deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="90420-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="90420-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90420-120">-DefaultProfile</span></span>
<span data-ttu-id="90420-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90420-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90420-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="90420-122">-FrontendProtocol</span></span>
<span data-ttu-id="90420-123">Einstellungen für frontend security-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="90420-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="90420-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="90420-124">This parameter is optional.</span></span>
<span data-ttu-id="90420-125">Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="90420-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="90420-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="90420-126">-ServerProtocol</span></span>
<span data-ttu-id="90420-127">Serverprotokolleinstellungen wie Http2.</span><span class="sxs-lookup"><span data-stu-id="90420-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="90420-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="90420-128">This parameter is optional.</span></span>
<span data-ttu-id="90420-129">Die gültigen Einstellungen sind `Http2` – Http 2.0 aktivieren</span><span class="sxs-lookup"><span data-stu-id="90420-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="90420-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90420-130">CommonParameters</span></span>
<span data-ttu-id="90420-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90420-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90420-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90420-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90420-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90420-133">INPUTS</span></span>

### <span data-ttu-id="90420-134">Keine</span><span class="sxs-lookup"><span data-stu-id="90420-134">None</span></span>

## <span data-ttu-id="90420-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90420-135">OUTPUTS</span></span>

### <span data-ttu-id="90420-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="90420-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="90420-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90420-137">NOTES</span></span>

## <span data-ttu-id="90420-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90420-138">RELATED LINKS</span></span>

[<span data-ttu-id="90420-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="90420-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

