---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176453"
---
# <span data-ttu-id="c676e-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c676e-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="c676e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c676e-102">SYNOPSIS</span></span>
<span data-ttu-id="c676e-103">Erstellt einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="c676e-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="c676e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c676e-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c676e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c676e-105">DESCRIPTION</span></span>
<span data-ttu-id="c676e-106">Erstellt einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="c676e-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="c676e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c676e-107">EXAMPLES</span></span>

### <span data-ttu-id="c676e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c676e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="c676e-109">Erstellt den Festplatten-Verschlüsselungs Satz mit dem angegebenen aktiven Schlüssel im Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="c676e-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="c676e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c676e-110">PARAMETERS</span></span>

### <span data-ttu-id="c676e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c676e-111">-AsJob</span></span>
<span data-ttu-id="c676e-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c676e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c676e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c676e-113">-DefaultProfile</span></span>
<span data-ttu-id="c676e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c676e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c676e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c676e-115">-InputObject</span></span>
<span data-ttu-id="c676e-116">Das lokale Objekt des Datenträger Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="c676e-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c676e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c676e-117">-Name</span></span>
<span data-ttu-id="c676e-118">Name des Festplatten-Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="c676e-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c676e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c676e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c676e-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c676e-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c676e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c676e-121">-Confirm</span></span>
<span data-ttu-id="c676e-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c676e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c676e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c676e-123">-WhatIf</span></span>
<span data-ttu-id="c676e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c676e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c676e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c676e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c676e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c676e-126">CommonParameters</span></span>
<span data-ttu-id="c676e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c676e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c676e-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c676e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c676e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c676e-129">INPUTS</span></span>

### <span data-ttu-id="c676e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c676e-130">System.String</span></span>

### <span data-ttu-id="c676e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c676e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c676e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c676e-132">OUTPUTS</span></span>

### <span data-ttu-id="c676e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c676e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c676e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c676e-134">NOTES</span></span>

## <span data-ttu-id="c676e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c676e-135">RELATED LINKS</span></span>
