---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946367"
---
# <span data-ttu-id="77737-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="77737-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="77737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77737-102">SYNOPSIS</span></span>
<span data-ttu-id="77737-103">Importieren Sie ein SSL-Zertifikat aus dem Schlüsseltresor in eine Web-App.</span><span class="sxs-lookup"><span data-stu-id="77737-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="77737-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77737-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77737-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77737-105">DESCRIPTION</span></span>
<span data-ttu-id="77737-106">Das **Cmdlet Import-AzWebAppKeyVaultCertificate** importiert ein SSL-Zertifikat aus dem Schlüsseltresor in eine Web-App.</span><span class="sxs-lookup"><span data-stu-id="77737-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="77737-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77737-107">EXAMPLES</span></span>

### <span data-ttu-id="77737-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77737-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="77737-109">Mit diesem Befehl wird ein SSL-Zertifikat aus dem Schlüsseltresor in eine Web-App importiert.</span><span class="sxs-lookup"><span data-stu-id="77737-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="77737-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="77737-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="77737-111">Mit diesem Befehl Importieren Eines SSL-Zertifikats aus dem Schlüsseltresor in eine Web App mithilfe der Ressourcen-ID (in der Regel, wenn sich der Schlüsseltresor in einem anderen Abonnement befindet).</span><span class="sxs-lookup"><span data-stu-id="77737-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="77737-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="77737-112">PARAMETERS</span></span>

### <span data-ttu-id="77737-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="77737-113">-CertName</span></span>
<span data-ttu-id="77737-114">KeyVaultCertName des zertifikats, das in keyvault erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="77737-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77737-115">-DefaultProfile</span></span>
<span data-ttu-id="77737-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77737-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77737-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="77737-117">-KeyVaultName</span></span>
<span data-ttu-id="77737-118">Der Name des Keyvaults.</span><span class="sxs-lookup"><span data-stu-id="77737-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77737-119">-ResourceGroupName</span></span>
<span data-ttu-id="77737-120">Der Name der WebApp-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="77737-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="77737-121">-Slot</span></span>
<span data-ttu-id="77737-122">Der Name des Webapp-Slot.</span><span class="sxs-lookup"><span data-stu-id="77737-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="77737-123">-WebAppName</span></span>
<span data-ttu-id="77737-124">Der Name der WebApp.</span><span class="sxs-lookup"><span data-stu-id="77737-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77737-125">-Confirm</span></span>
<span data-ttu-id="77737-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77737-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77737-127">-WhatIf</span></span>
<span data-ttu-id="77737-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77737-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77737-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77737-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77737-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77737-130">CommonParameters</span></span>
<span data-ttu-id="77737-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77737-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77737-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77737-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77737-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77737-133">INPUTS</span></span>

### <span data-ttu-id="77737-134">Keine</span><span class="sxs-lookup"><span data-stu-id="77737-134">None</span></span>

## <span data-ttu-id="77737-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77737-135">OUTPUTS</span></span>

### <span data-ttu-id="77737-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="77737-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="77737-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="77737-137">NOTES</span></span>

## <span data-ttu-id="77737-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="77737-138">RELATED LINKS</span></span>
