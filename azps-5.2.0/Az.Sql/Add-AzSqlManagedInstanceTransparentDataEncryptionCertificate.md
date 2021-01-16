---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293957"
---
# <span data-ttu-id="a18f6-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a18f6-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="a18f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a18f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a18f6-103">Fügt ein transparentes Datenverschlüsselungszertifikat für die angegebene verwaltete Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="a18f6-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="a18f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a18f6-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a18f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a18f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a18f6-106">Die Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein transparentes Datenverschlüsselungszertifikat für die angegebene verwaltete Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="a18f6-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="a18f6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a18f6-107">EXAMPLES</span></span>

### <span data-ttu-id="a18f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a18f6-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="a18f6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a18f6-109">PARAMETERS</span></span>

### <span data-ttu-id="a18f6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18f6-110">-DefaultProfile</span></span>
<span data-ttu-id="a18f6-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a18f6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18f6-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="a18f6-112">-ManagedInstanceName</span></span>
<span data-ttu-id="a18f6-113">Der Name der verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="a18f6-113">The managed instance name</span></span>

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

### <span data-ttu-id="a18f6-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a18f6-114">-PassThru</span></span>
<span data-ttu-id="a18f6-115">Gibt bei erfolgreicher Ausführung das hinzugefügte Zertifikatobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a18f6-115">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18f6-116">-Password</span><span class="sxs-lookup"><span data-stu-id="a18f6-116">-Password</span></span>
<span data-ttu-id="a18f6-117">Das Kennwort für das Zertifikat zur transparenten Datenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="a18f6-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18f6-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="a18f6-118">-PrivateBlob</span></span>
<span data-ttu-id="a18f6-119">Das private BLOB für transparente Datenverschlüsselungszertifikate</span><span class="sxs-lookup"><span data-stu-id="a18f6-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="a18f6-121">Der Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a18f6-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="a18f6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a18f6-122">-Confirm</span></span>
<span data-ttu-id="a18f6-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a18f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18f6-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a18f6-124">-WhatIf</span></span>
<span data-ttu-id="a18f6-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a18f6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a18f6-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a18f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18f6-127">CommonParameters</span></span>
<span data-ttu-id="a18f6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18f6-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a18f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18f6-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a18f6-130">INPUTS</span></span>

### <span data-ttu-id="a18f6-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a18f6-131">None</span></span>

## <span data-ttu-id="a18f6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a18f6-132">OUTPUTS</span></span>

### <span data-ttu-id="a18f6-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a18f6-133">System.Boolean</span></span>

## <span data-ttu-id="a18f6-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a18f6-134">NOTES</span></span>

## <span data-ttu-id="a18f6-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a18f6-135">RELATED LINKS</span></span>
